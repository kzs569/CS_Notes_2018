Quiz 2 - Week 3
===============

1、(5分)下列关于CISC和RISC的描述错误的是？

 A、 CISC指令长度是不固定的

 **B、 CISC指令的操作数必须预存于寄存器中**

 C、 RISC指令长度是固定的

 D、 RISC指令的操作数必须预存于寄存器中

 E、 RISC架构的指令种类通常比CISC架构更少


2、(5分)下列关于Intel处理器及其推出时间描述错误的是？

 A、 Intel 8086——1978年

 B、 Intel 80286——1982年

 C、 Intel Pentium——1993年

 D、 Intel PentiumPro——1995年

 **E、 Intel 80386——1988年 (1985年)**

 F、 Intel Core i7——2008年

 G、 Intel Core 2——2006年



3、(5分)x86体系结构中，寄存器EAX长度为多少位？

 A、 8位

 B、 16位

 **C、 32位**

 D、 64位


4、(5分)x86体系结构中，寄存器AX长度为多少位？

 A、 8位

 **B、 16位**

 C、 32位

 D、 64位


5、(5分)IA-32寄存器模型中包括以下哪些寄存器？（多选题）

 **A、 通用寄存器**

 **B、 指令指针寄存器**

 C、 页面寄存器

 **D、 标志寄存器**

 **E、 段寄存器**

6、(5分)8086系统中标志位CF的含义是？

 A、 溢出标志

 B、 零标志

 C、 符号标志

 **D、 进位标志**

**7、同第六题**

8、(5分)8086系统中标志位ZF的含义是？

 A、 符号标志 **(SF)**

 B、 奇偶标志 **(DF)**

 C、 溢出标志 **(OF)**

 D、 进位标志 **(CF)**

**E、 零标志**

9、(5分)8086系统中段寄存器DS的含义是？

 A、 代码段寄存器

 B、 附加段寄存器

 **C、 数据段寄存器**

 D、 堆栈段寄存器

10、(5分)8086系统中段寄存器CS的含义是？

 A、 数据段寄存器

 B、 附加段寄存器

 **C、 代码段寄存器**

 D、 堆栈段寄存器

11、(5分)设CS=2500H，DS=2400H，SS=2430H，BP=0200H，SI=0010H，DI=0206H，计算下列x86指令源操作数的物理地址：
MOV AX，[2000H]

 A、 4500H

 B、 27000H

 **C、 26000H**

 D、 4430H

注:mov ax,[idata] 含义：(ax)=((ds)*16 + idata)

12、(5分)设CS=2500H，DS=2400H，SS=2430H，BP=0200H，SI=0010H，DI=0206H，计算下列x86指令源操作数的物理地址：
MOV AX，[BP+SI+4]

 A、 2714H

 B、 25214H

 **C、 24514H**

 D、 2614H

注:mov ax,[bp+si+idata] 含义：(ax)=((ss)*16+(bp)+(si)+idata)

详见:http://www.cnblogs.com/huzhongzhong/archive/2011/08/01/2123743.html

13、(5分)设CS=2500H，DS=2400H，SS=2430H，BP=0200H，SI=0010H，DI=0206H，计算下列x86指令源操作数的物理地址：
MOV AX，[DI+100H]

 A、 25306H

 B、 24606H

 C、 2806H

 **D、 24306H**

 E、 2706H

 F、 2736H

注:mov ax,[di+idata] 含义：(ax)=((ds)*16+(di)+idata)

**14、同12题**

**15、同11题**

16、(5分)下列x86指令中，哪些属于算术运算指令？（多选题）

 **A、 ADD**

 **B、 DEC**

 C、 MOV

 D、 IN

 E、 LEA

 F、 AND

 G、 SHL

 H、 MOVSB

 I、 CALL

 J、 JNZ

 K、 LOOP

 **L、 MUL**

17、(5分)下列关于MIPS指令的主要特点说法错误的是？

 A、 指令长度固定

 B、 寻址模式简单

 C、 只有Load和Store指令可以访问存储器

 D、 需要优秀的编译器支持

 **E、 指令数量多，且功能复杂(CISC)**

18、(5分)MIPS按照指令的基本格式可以分为三种类型，以下不属于这三种类型的是？

 A、 R型指令

 **B、 O型指令**

 **C、 M型指令**

 D、 I型指令

 E、 J型指令

19、(5分)MIPS按照指令的基本格式进行划分，可以分为几种？

 A、 1

 B、 2

 **C、 3**

 D、 4

20、(5分)某MIPS指令的机器码是0x20A5FFFF，对应的汇编指令是什么？

 A、 addi $a2,$a2,-1

 B、 ori $a1,$a1,-1

 C、 ori $a2,$a2,-1

 **D、 addi $a1,$a1,-1**

注:[opcode文档](https://opencores.org/project/plasma/opcodes)

**0x20A5FFFF = 0010 0000 1010 0101 1111 1111 1111 1111**

 | opcode | rs | rt | imm|
 | ------ | ------| ------| ------ |
 | 001000|00101|00101|1111 1111 1111 1111|
 |addi|$a1|$a1|

21、(5分)某MIPS指令的机器码是0x0005402A，对应的汇编指令是什么？

 A、 slt $a1,$0,$t0

 B、 or $v0,$0,$a1

 C、 or $a1,$0,$v0

 **D、 slt $t0,$0,$a1**

注:**0x0005402A = 0000 0000 0000 0101 0100 0000 0010 1010**

 | opcode | rs | rt | rd|shamt|funct|
 | ------ | ------| ---|---| ------ | ------|
 | 000000|00000|00101|01000|00000|101010|
 |slt|$0|$a1|$t0|


22、(5分)阅读下面的x86汇编程序，回答问题。
; 设DS=1000H
``` vbscript
MOV SI, 1250H

MOV DI, 1370H

MOV CL, 3

MOV AX, DS

MOV ES, AX

MOV BX, 5

STD

REP MOVSB
```
请问，在这次串传送操作中，完成了第一个元素的传送后，SI寄存器的值是什么？

**A、 124FH**

 B、 1252H

 C、 1251

 D、 不确定

 |DF=0|DF=1|
 |---|---|
 |SI<-SI+1;DI<-DI+1|SI<SI-1;DI<-DI-1|

**23、同22题**

**24、同22题**

25、(5分)阅读下面的x86汇编程序，回答问题。
; 设DS=1000H
``` vbscript
MOV SI, 1250H

MOV DI, 1370H

MOV CL, 3

MOV AX, DS

MOV ES, AX

MOV BX, 5

CLD

REP MOVSB
```
请问，这次串传送操作，总共传送了多少个字节的数据？

 A、 0个

 B、 3个

 C、 5个

 **D、 不确定**(感觉是因为MOV BX,5的原因,因为此时CX值未知)

26、(5分)如果想用8086 CPU把内存中某个区域的1024个字节的数据传送到另一个区域，可以选用如下三种方法：
（1）只使用传送指令（MOV）；

（2）使用传送指令（MOV），并用条件转移指令建立循环语句的结构；

（3）使用串传送指令（MOVSB）以及必要的配合指令，不使用循环语句的结构。

请比较用这三种方法编写的程序，执行时访问存储器次数最少的是：

 A、 方法一

 B、 方法二

 **C、 方法三**

 D、 无法比较

27、(5分)如果想用8086 CPU把内存中某个区域的1024个字节的数据传送到另一个区域，可以选用如下三种方法：
（1）只使用传送指令（MOV）；

（2）使用传送指令（MOV），并用条件转移指令建立循环语句的结构；

（3）使用串传送指令（MOVSB）以及必要的配合指令，不使用循环语句的结构。

请比较用这三种方法编写的程序，执行时访问存储器次数最多的是：

 A、 方法一

 **B、 方法二**

 C、 方法三

 D、 无法比较

28、(5分)如果想用8086 CPU把内存中某个区域的1024个字节的数据传送到另一个区域，可以选用如下三种方法：
（1）只使用传送指令（MOV）；

（2）使用传送指令（MOV），并用条件转移指令建立循环语句的结构；

（3）使用串传送指令（MOVSB）以及必要的配合指令，不使用循环语句的结构。

请比较用这三种方法编写的程序，程序代码占用存储器空间最大的是：

 **A、 方法1**

 B、 方法2

 C、 方法3

 D、 无法比较

29、(5分)很多x86指令的功能比较复杂，往往一条x86指令可以完成的功能，需要多条MIPS指令才能实现。请问下列x86指令中，哪些确定能够只用一条MIPS指令完成对应的功能？（注：只需考虑这条指令本身，不用考虑对后续指令的影响）

 **A、 ADD ECX, 15H**

 **B、 MOV EAX, 28H**

 **C、 ADD EDX, EBX**

 D、 ADD EAX, [13H]

 E、 MOV EDX, [EBX+11H]

 F、 ADD [EBX+ESI*4+200H], EAX

 G、 REP MOVSB

 H、 JZ LOOP_1
