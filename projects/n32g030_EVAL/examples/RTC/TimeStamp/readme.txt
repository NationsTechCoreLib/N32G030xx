1、功能说明
    通过EXTI来触发时间戳。
    
2、使用环境

    软件开发环境：KEIL MDK-ARM V5.25

    硬件环境：
    1、基于评估板N32G030C8L7-STB V1.0开发
    2、MCU：N32G030C8L7

3、使用说明

    系统配置；
        1、时钟源：LSI
        2、EXTI：PB7
        3、串口配置：
                    - 串口为USART1（TX：PA9  RX：PA10）:
                    - 数据位：8
                    - 停止位：1
                    - 奇偶校验：无
                    - 波特率： 115200 
    使用方法：
    1、编译后烧录到评估板，上电后，给PB7灌入高电平，串口打印输出时间戳。

4、注意事项
    无
    
    
1. Function description

	1. The timestamp is triggered by the EXTI line.

2. Use environment

	Software development environment: KEIL MDK-ARM V5.25
	Hardware environment:
		1. based on the evaluation board N32G030C8L7-STB V1.0 development
		2. MCU: N32G030C8L7

3. Instructions for use

	System configuration:

		1. Clock source: LSI
		2. EXTI interrupt IO: PB7
		3. Serial port configuration:

							- Serial port: USART1 (TX: PA9 RX: PA10) :
							- Data bit: 8
							- Stop bit: 1
							- Parity check: None
							- Baud rate: 115200

	Instructions:
		1. After compiling, it is burned to the evaluation board. Power on, fill PB7 with high level , the serial port will print timestamp.

4. Matters needing attention
	None