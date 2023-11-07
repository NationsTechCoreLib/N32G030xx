1、功能说明

	1、SPI 全双工软件 NSS 模式发送接收数据

2、使用环境

	/* 软件开发环境：当前工程使用的软件工具名称及版本号 */
	IDE工具：KEIL MDK-ARM 5.30.0.0
	SDK版本：NNationstech.N32G030_Library.0.1.0

	/* 硬件环境：工程对应的开发硬件平台 */
	开发板：N32G030CL-STB V1.0 V1.0

3、使用说明
	
	/* 描述相关模块配置方法；例如:时钟，I/O等 */
	SystemClock：48MHz
	GPIO：SPI1: SCK--PA5、 MISO--PA6、 MOSI--PA7,
	           SPI2: SCK--PB13、MISO--PB14、MOSI--PB15，

	/* 描述Demo的测试步骤和现象 */
	1.编译后下载程序复位运行；
	2.SPI1 初始化位主机，发送数据，SPI2 初始化位丛机，接收数据 ，传输完成后，检查数据，查看 TransferStatus1 和 TransferStatus2 状态为 PASSED，
	  SPI2 初始化位主机，发送数据，SPI1 初始化位丛机，接收数据 ，传输完成后，检查数据，查看 TransferStatus3 和 TransferStatus4 状态为 PASSED；

4、注意事项
	无




1. Function description

	1. SPI full-duplex software NSS mode to send and receive data

2. Use environment

	/* Software development environment: the name and version number of the software tool used in the current project */
	IDE tool: KEIL MDK-ARM 5.30.0.0
	SDK version: NNationstech.N32G030_Library.0.1.0

	/* Hardware environment: the development hardware platform corresponding to the project */
	Development board: N32G030CL-STB V1.0 V1.0

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	SystemClock: 48MHz
	GPIO: SPI1: SCK--PA5, MISO--PA6, MOSI--PA7,
	          SPI2: SCK--PB13, MISO--PB14, MOSI--PB15,

	/* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. SPI1 initializes the bit host, sends data, SPI2 initializes the bit cluster machine, receives data, after the transmission is completed, 
	    check the data, check that the status of TransferStatus1 and TransferStatus2 is PASSED,
	    SPI2 initializes the bit host, sends data, SPI1 initializes the bit cluster machine, receives data, and after the transmission is completed,
	    check the data, and check that the status of TransferStatus3 and TransferStatus4 is PASSED;

4. Matters needing attention
	none