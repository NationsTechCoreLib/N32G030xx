1、功能说明

	1、I2S 主模式发送数据完成以后切换成 SPI 主模式发送数据，再切换成 I2S 从模式发送数据。

2、使用环境

	/* 软件开发环境：当前工程使用的软件工具名称及版本号 */
	IDE工具：KEIL MDK-ARM 5.30.0.0
	SDK版本：NNationstech.N32G030_Library.1.1.1

	/* 硬件环境：工程对应的开发硬件平台 */
	开发板：N32G030CL-STB V1.0 V1.1

3、使用说明
	
	/* 描述相关模块配置方法；例如:时钟，I/O等 */
	1、SystemClock：48MHz
	2、GPIO：（主模式 DEMO 板）I2S1: WS--PA4、CK--PA5、SD--PA7
	         （从模式 DEMO 板）I2S1: WS--PA4、CK--PA5、SD--PA7

	/* 描述Demo的测试步骤和现象 */
	1.编译后下载程序复位运行；
	2.从模式 DEMO 板进入调试模式，先按住主模式 DEMO 板复位键，然后从模式 DEMO 板全速跑，再松开主模式 DEMO 板复位键。

4、注意事项
	需要两块 demo 板配合，一块板子烧录主模式程序，一块板子烧录从模式程序，连接两块板子的 VCC 和 GND。


1. Function description

	1. After I2S master mode sends data, switch to SPI master mode to send data, and then switch to I2S slave mode to send data

2. Use environment

	/* Software development environment: the name and version number of the software tool used in the current project */
	IDE tool: KEIL MDK-ARM 5.30.0.0
	SDK version: NNationstech.N32G030_Library.1.1.1

	/* Hardware environment: the development hardware platform corresponding to the project */
	Development board: N32G030CL-STB V1.0 V1.1

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	1. SystemClock: 48MHz
	2. GPIO: (main mode DEMO board)  I2S1: WS--PA4, CK--PA5, SD--PA7
	         (Slave mode DEMO board) I2S1: WS--PA4, CK--PA5, SD--PA7

	/* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. Enter the debug mode from the mode DEMO board, first press and hold the main mode DEMO board reset button, 
	   then run the slave mode DEMO board at full speed, then release the main mode DEMO board reset button.

4. Matters needing attention
	Two demo boards are needed, one board to program the master mode program, one board to program the slave mode program,
	connect the VCC and GND of the two boards.