# 计算机组成原理

## 第一章　计算机系统概论

### 1.3.1 硬件组成要素

- 相当于算盘功能的部件，我们称之为<font color = "1E90FF">运算器</font>；相当于纸那样具有“记忆”功能的部件我们称之为<font color = "1E90FF">存储器</font>；相当于笔那样把原始解题信息送到计算机或把计算机结果显示出来的设备，我们称之为<font color = "1E90FF">输入设备</font>或<font color = "1E90FF">输出设备</font>；而相当于人的大脑能够自动控制整个计算过程的，称之为<font color = "1E90FF">控制器</font>。图1.2所示为数字计算机的主要组成结构，其中双线及箭头表示数据代码传送通路。

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="../images/1-2.png" height="600px">
    <br>
    <div style="color:orange;border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">图1-2&emsp;数字计算机主要组成结构</div>
</center>




### 1.3.2 运算器

- 运算器就好像是由电子线路组成的算盘，图1.3是它的示意图。它的功能主要是进行加、减、乘、除等算数运算。除此之外，还可以进行逻辑运算，因此通常称为**ALU**(算数逻辑运算部件)。

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="../images/1-3.png" height="300px">
    <br>
    <div style="color:orange;border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">图1-3&emsp;运算器结构示意图</div>
</center>

### 1.3.3 存储器

- 存储器的功能是保存或“记忆”解题的原始数据和解题步骤。为此再运算前需要把参加运算的数据和解题步骤通过输入设备送到存储器中保存起来。
- 通常，在存储器中把保存一个数的16个触发器称为一个<font color = "1E90FF">存储单元</font>。存储器是由许多存储单元组成的。每个存储单元都有编号，称为<font color = "1E90FF">地址</font>。向存储器中



<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="../images/1-4.png" height="300px">
    <br>
    <div style="color:orange;border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">图1-4&emsp;存储器结构示意图</div>
</center>

## 第二章 运算方法和运算器
### 计算题节选

- 12. 用`IEEE 32`位浮点格式表示如下的数

  (1) $-5$ (2) $-1.5$ (3) $384$ (4) <font size = 4>$\frac{1}{16}$</font> (5) <font size = 4>$-\frac{1}{32}$</font>

(1)先转化为2进制，$(-5)_{10} = (-101)_{2}$

∴$S = 1$ 

然后移动移动小数点，使其在1、2位之间
$$
1.01 \times 2^2 \qquad e=2
$$
于是得到
$$
S=1,E=2+127=129, \qquad M=01
$$
最后得到32位浮点数的二进制存储格式为
$$
{\color{red}1}{\color{green}100\,0000\,1}010\,0000\,0000\,0000\,0000\,0000=(C0A00000)_{16}\\
*红色是符号位，绿色是阶码
$$

(2)先转化为2进制，$(-1.5)_{10} = (-1.1)_{2}$

∴$S = 1$ 

然后移动移动小数点，使其在1、2位之间
$$
1.1 \times 2^0 \qquad e = 0
$$
于是得到
$$
S=1,E=0+127=127, \qquad M=1
$$
最后得到32位浮点数的二进制存储格式为
$$
{\color{red}1}{\color{green}011\,1111\,1}100\,0000\,0000\,0000\,0000\,0000=(BFC00000)_{16}\\
*红色是符号位，绿色是阶码
$$












