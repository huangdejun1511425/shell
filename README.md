# Introduction
A simple simulation of shell in Linux for learning.
A blog (in Chinese) of introduction and how to build it :http://www.cnblogs.com/wuyuegb2312/p/3399566.html

# Usage
type

　　make wshell

for wshell read input by fgets() or

　　make wshell_r
　　

for wshell with readline lib.It need to install libreadline5-dev first.


## Attention

　　Because of the lack of support for regular expressions , typing file's names such as "*.c" are not support.
　　

# File List
### wshell.c
　　main program

### type_prompt.c
　　print out the prompt of wshell including path,hostname

### read_command.c
　　read command input, and analyse the command and parameter(s).

### builtin_command.c
　　support some built-in command,such as exit,quit,about, and cd.

### test.c
　　a test program, helloworld, which can be executed in wshell.

### parsing.c
　　analyses user's input line and tell them to wshell


# 用法
输入

　　make wshell

构建使用fgets()接收命令的wshell

　　make wshell_r
　　

构建使用readline接收命令的wshell。需要安装libreadline5-dev或其他类似的库。

　　

# 文件列表
### wshell.c
　　主程序

### type_prompt.c
　　拼接当前路径、主机名的提示符。

### read_command.c
　　读取输入的命令，并分离出其中的参数。

### builtin_command.c
　　提供对基本内建命令的支持，含exit、quit、about、cd等。

### test.c
　　用来在wshell中执行的测试程序。

### parsing.c
　　分析用户输入（是否使用了管道、重定向、后台执行等）。

