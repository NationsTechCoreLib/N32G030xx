1、功能说明
    1、SLEEP进入和唤醒退出示例。


2、使用环境

    软件开发环境：KEIL MDK-ARM V5.25

    硬件环境：
        1、基于评估板N32G030C8L7-STB V1.0开发
        2、MCU：N32G030C8L7


3、使用说明

    系统配置；
        1、时钟源：HSE+PLL


    使用方法：
        在KEIL下编译后烧录到评估板，上电输出打印“PWR_SLEEP INIT”。过了一会输出打印“Lower Power Entry”，表明进入SLEEP了。
        按下WAKEUP按键后，串口输出“Lower Power Exit”，表明MCU被唤醒。


4、注意事项
    无


1. Function description
    1. Example of SLEEP entry and wake-up exit.

2. Use environment

    Software development environment:
        IDE tool: KEIL MDK-ARM V5.25
      
    Hardware environment:
        Development board: N32G030C8L7-STB V1.0
        MCU：N32G030C8L7

3. Instructions for use

    System Configuration;
        1. Clock source: HSE+PLL

    Instructions:
        After compiling under KEIL and burning it to the evaluation board, the output prints "PWR_SLEEP INIT" after power-on. After a while, the output prints "Lower Power Entry", indicating that it has entered SLEEP.
        After pressing the WAKEUP button, the serial port outputs "Lower Power Exit" again, indicating that the MCU is awakened.


4. Matters needing attention
    none
