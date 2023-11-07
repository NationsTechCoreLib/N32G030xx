1、功能说明

	1、SPI 从模式全双工 DMA 发送和单线接收数据

2、使用环境

	/* 软件开发环境：当前工程使用的软件工具名称及版本号 */
	IDE工具：KEIL MDK-ARM 5.30.0.0
	SDK版本：Nationstech.N32G030_Library.0.1.0

	/* 硬件环境：工程对应的开发硬件平台 */
	开发板：N32G030CL-STB V1.0 V1.0

3、使用说明
	
	/* 描述相关模块配置方法；例如:时钟，I/O等 */
	SystemClock：48MHz
	GPIO：（主模式 DEMO 板）SPI1: SCK--PA5、MISO--PA6、MOSI--PA7,
	           （从模式 DEMO 板）SPI1: SCK--PA5、MISO--PA6、MOSI--PA7,
	日志打印：从模式 DEMO 板 PA9(TX)，波特率：115200

	/* 描述Demo的测试步骤和现象 */
	1、编译后下载程序复位运行；
	2、接好串口打印工具，上电，查看打印测试成功

4、注意事项
	需要两块 demo 板配合，一块板子烧录主模式程序，一块板子烧录从模式程序，两块板子需一起上电，连接两块板子的 VCC 和 GND




1. Function description

	1. SPI slave mode full-duplex DMA transmit and single-wire receive data

2. Use environment

	/* Software development environment: the name and version number of the software tool used in the current project */
	IDE tool: KEIL MDK-ARM 5.30.0.0
	SDK version: Nationstech.N32G030_Library.0.1.0

	/* Hardware environment: the development hardware platform corresponding to the project */
	Development board: N32G030CL-STB V1.0 V1.0

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	SystemClock: 48MHz
	GPIO: (master mode DEMO board) SPI1: SCK--PA5, MISO--PA6, MOSI--PA7,
	             (Slave mode DEMO board) SPI1: SCK--PA5, MISO--PA6, MOSI--PA7,
	Log print: slave mode DEMO board PA9(TX), baud rate: 115200

	/* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. Connect the serial port printing tool, power on, and check that the printing test is successful

4. Matters needing attention
	Two demo boards are required, one board to program the master mode program, one board to program the slave mode program,
	 the two boards need to be powered on together, and connect the VCC and GND of the two boards.