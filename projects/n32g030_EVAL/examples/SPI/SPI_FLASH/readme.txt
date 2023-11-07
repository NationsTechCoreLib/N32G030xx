1、功能说明

	1、SPI 读、写、擦除 W25Q128

2、使用环境

	/* 软件开发环境：当前工程使用的软件工具名称及版本号 */
	IDE工具：KEIL MDK-ARM 5.30.0.0
	SDK版本：Nationstech.N32G030_Library.0.1.0

	/* 硬件环境：工程对应的开发硬件平台 */
	开发板：N32G030CL-STB V1.0 V1.0

3、使用说明
	
	/* 描述相关模块配置方法；例如:时钟，I/O等 */
	1、SystemClock：48MHz
	2、SPI1: NSS--PA4、SCK--PA5、MISO--PA6、MOSI--PA7

	/* 描述Demo的测试步骤和现象 */
	1、编译后下载程序复位运行；
	2、通过 SPI1 读取 W25Q128 的 ID，然后写数据，再读出来，比较读写数据，查看 TransferStatus1 状态为 PASSED，然后擦除块，检查擦除块正常。

4、注意事项
	将 N32G030CL-STB V1.0 V1.0 开发板上的 SPI1 接口接在 N32G457QE_EVB 开发板的 W25Q128 上，两个开发板需要共地。




1. Function description

	1. SPI read, write, erase W25Q128

2. Use environment

	/* Software development environment: the name and version number of the software tool used in the current project */
	IDE tool: KEIL MDK-ARM 5.30.0.0
	SDK version: Nationstech.N32G030_Library.0.1.0

	/* Hardware environment: the development hardware platform corresponding to the project */
	Development board: N32G030CL-STB V1.0 V1.0

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	1. SystemClock: 48MHz
	2. SPI1: NSS--PA4, SCK--PA5, MISO--PA6, MOSI--PA7

	/* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. Read the ID of W25Q128 through SPI1, then write the data, then read it out, compare the read and write data, 
	    check that the status of TransferStatus1 is PASSED, then erase the block, and check that the erase block is normal.

4. Matters needing attention
	Connect the SPI1 interface of the N32G030CL-STB V1.0 V1.0 development board to the W25Q128 of the N32G457QE_EVB development board. 
	The two development boards need to share the ground.