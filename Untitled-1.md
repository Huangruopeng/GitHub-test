---
export_on_save:
  pandoc: true
  ---
title: "Habits"
output:
  pdf_document:
  path: /desktop/Habits.pdf
   
---

---

# 这是 <h1> 一级标题
## 这是 <h2> 二级标题
### 这是 <h3> 三级标题
#### 这是 <h4> 四级标题
##### 这是 <h5> 五级标题
###### 这是 <h6> 六级标题
 
* 这是点 还得有空格

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

* [这是 <h1> 一级标题](#这是-h1-一级标题)
	* [这是 <h2> 二级标题](#这是-h2-二级标题)
		* [这是 <h3> 三级标题](#这是-h3-三级标题)
			* [这是 <h4> 四级标题](#这是-h4-四级标题)
				* [这是 <h5> 五级标题](#这是-h5-五级标题)
					* [这是 <h6> 六级标题](#这是-h6-六级标题)

<!-- /code_chunk_output -->

*斜体*

*这会是 斜体*

_这会是 斜体 的文字_

**这会是 粗体 的文字**
__这会是 粗体 的文字__

_你也 **组合** 这些符号_

~~这个文字将会被横线删除~~

* Item 1
* Item 2
  * Item 2a
  * Item 2b
    * Item 3a
    * Item 3b


1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b
      1. Item 4a

          ![avatar](/Users/Rocair/Desktop/1.png)

           ![avatar](https://images2015.cnblogs.com/blog/818978/201603/818978-20160330232818082-562710541.png)



[*GitHub*](http://github.com)

正如 Kanye West 所说：

> We're living the future so
> the present is our past.

如下，三个或者更多的

------

连字符

*****

星号

___

下划线
   
```c {.line-numbers}
   #include<stdlib.h>
   #include<stdio.h>
   int main()
   {
     printf("Hello World" );
   }
```

```matlab {.line-numbers}
  A=[1:10:0.1]
  B=2.*A;
  plot(A,B);
```

- [x] @mentions, #refs, [links](http://github.com), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

First Header |Second Header|Third Header 
------------ | -------------|----------
Content from cell 1 |  Content from cell 2
Content in the first column | Content in the second column

:smile::fa-car:
:cry:
:train:

 The 30^th^ research.

 Content [^1]
 Content [^2]

[^1]: Hi! This is a footnote 
[^2]: This is my first time to use markdown
 
*[HTML]: Hyper Text Markup Language
*[W3C]:  World Wide Web Consortium
The HTML specification
is maintained by the W3C.

==marked there exist a sentence.==

$f(x)=sin(x)+2x$
$f(x)=x/(x^2+5x)$
$$\sum_{n=1 }^{100}x^2 +(7/x^4)$$
        
 @import "1.png" {width="300px" height="200px" title=" my screen shot" alt="我的 桌面"}

 ```gnuplot {cmd=true output="html"}
set terminal svg
set title "Simple Plots" font ",20"
set key left box
set samples 50
set style data points

plot [-10:10] sin(x),atan(x),cos(atan(x))
```

```python {cmd=true matplotlib=true}
import matplotlib.pyplot as plt
plt.plot([1,2,3, 4])
plt.show() # show figure
```

