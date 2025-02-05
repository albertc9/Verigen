# Verigen
A Verilog Generate Anything Tool

Verigen这个开源工具的操作逻辑如下：

1. 单独输入`verigen`时：进入一个操作环境（如输入python或输入root一样，在terminal中进入一个操作环境，这里有预先下载好的iverilog, yosys, netlistsvg（后文统称verigen套件(verigen tools)），从而我可以在外部没有预先安装这些工具的情况下运行指令。在这个环境内，一切命令如故，就好像进入了一个装有以上工具的conda容器一样（除了没有用户名，以及将每一句命令的开头换成'>'。设计一个简单的欢迎界面，用于提示版本等信息。输入`.q`即可退出环境。
2. 在预装了verigen套件的terminal中，或者在verigen环境中：输入格式形如`verigen dut.v testbench.v`或`verigen testbench.v dut.v`时，执行`iverilog`的模拟命令，生成一个中间`simv`文件后，直接自动完成模拟，然后删除中间文件`simv`。也就是说，不需要多步操作，只需要一个命令即可完成模拟。
3. 在预装了verigen套件的terminal中，或者在verigen环境中：输入格式形如`verigen dut.v`或`verigen -a dut.v`或`verigen -all dut.v`，则输出`.json`和`.svg`两个文件；如果添加参数`verigen -j dut.v`，只输出`.json`文件；如果添加参数`verigen -s dut.v`，在输出`.json`和`.svg`后，删除`.svg`文件。
