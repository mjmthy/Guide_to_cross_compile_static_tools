# 简介

&ensp;&ensp;&ensp;&ensp;trace-cmd是ftrace的一个前端，可以简化ftrace的使用

# 代码获取

&ensp;&ensp;&ensp;&ensp;$ git clone git://git.kernel.org/pub/scm/utils/trace-cmd/trace-cmd.git

# 代码编译

&ensp;&ensp;&ensp;&ensp;解压源码并进入顶层目录后，执行如下命令编译

&ensp;&ensp;&ensp;&ensp;$ make LDFLAGS=-static CC=/opt/gcc-arm-8.3-2019.03-x86_64-arm-linux-gnueabihf/bin/arm-linux-gnueabihf-gcc trace-cmd

&ensp;&ensp;&ensp;&ensp;编译结束后，可以在tracecmd目录下找到静态链接的可执行文件trace-cmd

<div align="center"><img src="images\compile.png"></div>

<p align="center">P1. 编译</p>

# 验证

&ensp;&ensp;&ensp;&ensp;这里结合kernelshark验证，具体如下图所示：

<div align="center"><img src="images\verify.png"></div>

<p align="center">P2-a. 通过trace-cmd抓取数据</p>

<div align="center"><img src="images\verify_2.png"></div>

<p align="center">P2-b. 通过kernelshark可视化观察抓获的数据</p>