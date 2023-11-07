1. 功能说明
    此例程展示蜂鸣器模块的用法

2. 使用环境
    软件开发环境: KEIL MDK-ARM 5.26
    硬件环境：     N32G030C8L7-STB V1.0

3. 使用说明
    描述相关模块配置方法；例如:时钟，I/O等 
         1. 时钟源：HSE+PLL
         2. 主时钟：48MHz
         3. GPIO：PA6--AF_PP, PA7--AF_PP

    描述Demo的测试步骤和现象 
         1. 编译后下载程序复位运行
         2. 用示波器查看波形，验证结果

4. 注意事项
    1、PA6与PA7的波形互补
    2、此例程是3603-1A蜂鸣器例程，相应的驱动、工程与其他有所更改（寄存器不一样），注意使用当前最新的pack包（1.0.1版本及以上）
    3、支持进入LPRUN模式，此时输出频率为pclk1的4分频值
    4、APB时钟频率选择寄存器位（freq_sel）的值根据主频而定，起到输出波形不至于失真的效果

1. Function description
    This routine shows the use of the beeper module

2. Use environment
    Software environment:  KEIL MDK-ARM 5.26
    Hardware environment: N32G030C8L7-STB V1.0

3. Instructions for use
    Describe the configuration method of related modules; for example: clock, I/O, etc. 
        1. Clock source: HSE+PLL
        2. Main clock: 48MHz
        3. GPIO: PA6--AF_PP, PA7--AF_PP
                  
    Describe the test steps and phenomena of Demo 
        1. After compiling, download the program to reset and run;
        2. Use oscilloscope to view the waveform and verify the result
 
4. Matters needing attention
    1. Waveforms of PA6 and PA7 are complementary
    2. This routine is 3603-1A beeper routine, the corresponding driver, project and other changes (register is not the same), pay attention to the use of the current latest pack pack (version 1.0.1 and above)
    3. Support to enter the LPRUN mode, at this time the output frequency is pCLK1 4 division value
    4. The value of APB clock frequency selection register bit (freq_SEL) is determined according to the main frequency, so that the output waveform will not be distorted