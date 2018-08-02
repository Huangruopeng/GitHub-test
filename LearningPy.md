# Learning Python
 August 2018
 Before this summer session, I found some MOOC videos and ebooks about Python. And I want to record this learning process with markdown and GitHub. :joy:

 # Content
 ## 1 Learing sources
 ### 1.1 MOOC Videos
*  Python程序设计教学精品课 _https://www.icourse163.org/course/BIT-268001_
*  Python网络爬虫与信息提取 _https://www.icourse163.org/course/BIT-1001870001?tid=1002236011_
 ### 1.2  Text books
 * Learning Python 5th Edition  writhen by  *Mark* _Lutz_ &nbsp;&nbsp;&nbsp;&nbsp; [*Learning Python 5th Edition*](https://books.google.com.hk/books?id=4pgQfXQvekcC&printsec=frontcover&dq=learning+python&hl=zh-CN&sa=X&redir_esc=y&sourceid=cndr#v=onepage&q=learning%20python&f=false)

 * Python official documentation &nbsp;&nbsp;&nbsp;&nbsp;[*The Python Tutorial*](https://docs.python.org/3/tutorial/)
  
## 2 Introduction
### 2.1 General Intro
  Python，是一种广泛使用的高级编程语言，属于通用型编程语言，由吉多·范罗苏姆创造，第一版发布于1991年。可以视之为一种改良的LISP。作为一种解释型语言，Python的设计哲学强调代码的可读性和简洁的语法。相比于C++或Java，Python让开发者能够用更少的代码表达想法。
   ![Python](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1533203810376&di=f19640034cd784d26a96dbadc33b4153&imgtype=0&src=http%3A%2F%2Fstatic.open-open.com%2Flib%2FuploadImg%2F20160623%2F20160623173015_416.png)
### 2.2 Characters
#### 2.2.1 Software quality
&emsp;For many, Python’s focus on readability, coherence, and software quality in general sets it apart from other tools in the scripting world. Python code is designed to be readable, and hence reusable and maintainable—much more so than traditional scripting languages. The uniformity of Python code makes it easy to understand, even if you did not write it. In addition, Python has deep support for more advanced software reuse mechanisms, such as object-oriented (OO) and function programming.
#### 2.2.2 Developer productivity
&emsp;Python boosts developer productivity many times beyond compiled or statically typed languages such as C, C++, and Java. Python code is typically one-third to 3 one-fifth the size of equivalent C++ or Java code. That means there is less to type, less to debug, and less to maintain after the fact. Python programs also run immediately, without the lengthy compile and link steps required by some other tools, further boosting programmer speed.
#### 2.2.3 Program portability
&emsp;Most Python programs run unchanged on all major computer platforms. Porting Python code between Linux and Windows, for example, is usually just a matter of copying a script’s code between machines. Moreover, Python offers multiple options for coding portable graphical user interfaces, database access programs, webbased systems, and more. Even operating system interfaces, including program launches and directory processing, are as portable in Python as they can possibly be.
#### 2.2.4 Support libraries
&emsp;Python comes with a large collection of prebuilt and portable functionality, known as the standard library. This library supports an array of application-level programming tasks, from text pattern matching to network scripting. In addition, Python can be extended with both homegrown libraries and a vast collection of third-party application support software. Python’s third-party domain offers tools for website construction, numeric programming, serial port access, game development, and much more (see ahead for a sampling). The NumPy extension, for instance, has been described as a free and more powerful equivalent to the Matlab numeric programming system.
#### 2.2.5 Component integration
&emsp;Python scripts can easily communicate with other parts of an application, using a variety of integration mechanisms. Such integrations allow Python to be used as a product customization and extension tool. Today, Python code can invoke C and C++ libraries, can be called from C and C++ programs, can integrate with Java and .NET components, can communicate over frameworks such as COM and Silverlight, can interface with devices over serial ports, and can interact over networks with interfaces like SOAP, XML-RPC, and CORBA. It is not a standalone tool.



## 3 Learning Process
### 3.1 Basic syntax elements of python
  Example from the MOOC <font color=DodgerBlue size=3>_TemperatureConvert_</font> 
   **Source Code**
   ```python {.line-numbers}
       #TempConvert.py
    TempStr = input("请输入带有符号的温度值: ")
    if TempStr[-1] in ['F', 'f']:
        C = (eval(TempStr[0:-1]) - 32)/1.8
        print("转换后的温度是{:.2f}C".format(C))
    elif TempStr[-1] in ['C', 'c']:
        F = 1.8*eval(TempStr[0:-1]) + 32
        print("转换后的温度是{:.2f}F".format(F))
    else:
        print("输入格式错误")

   ```
主体结构就是if-else语句
**缩进(indentation)**
* **严格明确**：缩进是语法的一部分，缩进不正确程序运行错误
* **所属关系**：表达代码间包含和层次关系的唯一手段
* **长度一致**：程序内一致即可，一般用4个空格或1个Tab</br>
     :bulb:<font color=DimGray size=3>_学到这里感觉头一次感到缩进对代码的重要性，以前写C/C++,MatLab和VHDL时还真没遇到过因为缩进出现的Bug，只是认为缩进只是为了阅读方便而已，因为这些语言都会有特定的字符来确定程序的结构。比如C/C++会有“{  }”来避免由于缩进导致的Bug，Matlab和VHDL在if语句中也会有end if 来结尾，Python竟然靠缩进！ 也许是还没深入学习（可能到后面会有不一样的理解）。_</font> 

**注释(Comment)**
* **单行注释**：以#开头，其后内容为注释
* **多行注释**：：以 ''' 开头和结尾
  ```python
  ''' 这是多行注释
     一个开头
     一个结尾
  '''
   ```

**变量(Variable)**
* 变量采用标识符(名字)来表示，关联标识符的过程叫命名</br>
  &emsp; TempStr 是变量名字
* 可以使用等号 (=) 向变量赋值或修改， =被称为赋值符号</br>
  &emsp;TempStr = "82F "#向变量 TempStr 赋值 "82F "</br>
:bulb:<font color=DimGray size=3>_It's like MatLab, needn't to preclaim the variable._</font>

**Name**
* **Naming rules**: Uppercase and lowercase letters, underline and Chinese characters and combinations.
* **Tips**: Case sensitive, the first character cannot be the number and is not the same as a reserved word.
   Python and python are different variables, 123Python is illegal

***
**And So on**</br>
:bulb:<font color=DimGray size=3>_It's waste a lot of my time to summarize the basics. You can find similar points from many websites。_</font>
  
  




    




 
