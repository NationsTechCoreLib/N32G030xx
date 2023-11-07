1、功能说明
    通过PC13来检测入侵。

2、使用环境

    软件开发环境：KEIL MDK-ARM V5.25

        硬件环境：
        1、基于评估板N32G030C8L7-STB V1.0开发
        2、MCU：N32G030C8L7

3、使用说明

    系统配置；
        1RTC时钟：LSI
        2入侵检测口：PC13
        3、串口配置：
                    - 串口为USART1（TX：PA9  RX：PA10）:
                    - 数据位：8
                    - 停止位：1
                    - 奇偶校验：无
                    - 波特率： 115200 
    使用方法：
        1、编译后烧录到评估板，上电后，给PC13外接下拉，PC13注入高电平，串口打印输出Tamper interrupt。
                
4、注意事项
    无  
    
1. Function description

	1. Tamper is triggered by detecting PC13 IO.

2. Use environment

	Software development environment: KEIL MDK-ARM V5.25
	Hardware environment:
		1. based on the evaluation board N32G030C8L7-STB V1.0 development
		2. MCU: N32G030C8L7

3. Instructions for use

	System configuration:

		1. RTC Clock source: LSI
        2. Tamper detection IO: PC13
		3. Serial port configuration:
							- Serial port: USART1 (TX: PA9 RX: PA10) :
							- Data bit: 8
							- Stop bit: 1
							- Parity check: None
							- Baud rate: 115200

	Instructions:
		1. After compiling, it is burned to the evaluation board. After powering on, connect PC13 to the external pull-up, high level is artificially injected into PC13 and "Tamper interrupt" is output through the serial port. 
        
4. Matters needing attention
	None