# FPGAforDL

on FPGA to deploy a deep neural network.

## workflows

### 第一阶段：FPGA 与 DL 相关技能技术调研

- 时间：1.28.2023-2.11.2023

- 关键结果：
  - 阅读相关文献，查找 FPGA 在 DL 领域的应用案例，记录并总结各个方案的优缺点
  - 确定具体项目实施目标及之后开展的规划
  - 总结前期需要的基础技术栈

### 第二阶段：搭建实验环境与流水灯的实现
一、搭建环境
  -Vivado下载：下载链接：https://www.xilinx.com/support/download.html 选择2018.3版本。.lic文件可从百度获取
  -Modelsim下载：按照流程即可，破解软件时需注意，用管理员身份运行.bat文件失败时，可尝试直接运行。环境变量创建失败时，将变量名称改为MGLS_LICENSE_FILE。
  -Midelsim与Vivado关联：创建所需文件，按流程即可。
  
 二、LED灯实验
  -创建工程：按流程即可
  -程序设计：1.新建并添加.v文件，结合电路原理图，选用Verilog编程。2.添加管脚约束，新建并添加.xdc文件，参考Xilinx相关文档编写代码。
  3.生成.bit文件,点击program and debug里的Generate Bitstream。
  -下载验证：1.将板子接入电脑，选择自动连接。 2.在program device里找到bit的文件的所在位置，点击Program按钮下载程序。
