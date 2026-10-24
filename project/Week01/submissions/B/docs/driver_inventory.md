# 现有工程阅读记录

现有固件放在02_驱动工程/CampusCatFeederESP32目录。第一周先认清文件和入口，后面修改时知道该从哪里查，不把整套驱动当作本周新写的代码。

|文件或目录|主要内容|
|---|---|
|CampusCatFeederESP32.ino|主程序，负责读取模块、处理串口命令和控制投喂流程|
|src/FeederConfig.h|引脚、串口以及投喂相关的配置|
|src/Hx711Reader.h和.cpp|HX711称重读数|
|src/ServoGate.h和.cpp|舵机控制|
|src/HUSKYLENS/|已有的HUSKYLENS官方通信库|
|src/SafetyPolicy.h|可单独检查的部分策略函数|
|tests/safety_policy_test.cpp|原有主机测试入口|
|bench/ServoBenchESP32/ServoBenchESP32.ino|舵机单独测试用的程序|
|README.md|工程说明、接线和操作方法|

从结构上看，主程序把识别、称重、按钮和舵机串在一起。后续排查问题时，先判断是模块读写出了问题，还是投喂条件和状态转换没有满足。测试程序虽然已经存在，但第一周的附件只记录入口，没有据此填写本周测试通过。

下周先把开发环境配好，尝试复现编译；再与赵振翔核对需求对应的代码，与刘营鑫确认仿真需要哪些输入。实际修改的文件和编译输出到时另存记录。
