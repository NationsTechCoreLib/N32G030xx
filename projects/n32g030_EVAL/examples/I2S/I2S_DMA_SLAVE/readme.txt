1、功能说明

	1、I2S 从模式通过 DMA 收发数据

2、使用环境

        /* 软件开发环境：当前工程使用的软件工具名称及版本号 */
        IDE工具：KEIL MDK-ARM 5.30.0.0
        SDK版本：Nationstech.N32G030_Library.1.1.1

        /* 硬件环境：工程对应的开发硬件平台 */
        开发板：N32G030CL-STB V1.0 V1.1

3、使用说明
	
	/* 描述相关模块配置方法；例如:时钟，I/O等 */
        1、SystemClock：48MHz
        2、GPIO：（主模式 DEMO 板）I2S1: WS--PA4、CK--PA5、SD--PA7
	             （从模式 DEMO 板）I2S1: WS--PA4、CK--PA5、SD--PA7
        3、DMA：I2S1 发送采用 DMA_CH3 通道，I2S1 接收采用 DMA_CH2 通道；
        4、日志打印：从模式 DEMO 板 PA9(TX)，波特率：115200
	
         /* 描述Demo的测试步骤和现象 */
        1、编译后下载程序复位运行；
        2、主模式 DEMO 板和从模式 DEMO 板PA4,PA5,PA7连接好后，从模式 DEMO 板连接串口打印工具，上电，
           先按住主模式 DEMO 板复位键不松，再按下从模式 DEMO 板的复位键，从模式 DEMO 板跑起来后再松开主模式 DEMO 板的复位键，查看打印测试成功；

4、注意事项
	需要两块 demo 板配合，一块板子烧录主模式程序，一块板子烧录从模式程序，两块板子需一起上电，连接两块板子的 VCC 和 GND



1. Function description

	1. I2S slave mode sends and receives data through DMA

2. Use environment

        /* Software development environment: the name and version number of the software tool used in the current project */
        IDE tool: KEIL MDK-ARM 5.30.0.0
        SDK version: Nationstech.N32G030_Library.1.1.1

        /* Hardware environment: the development hardware platform corresponding to the project */
        Development board: N32G030CL-STB V1.0 V1.1

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	1. SystemClock: 48MHz
	2. GPIO: (main mode DEMO board) I2S1: WS--PA4, CK--PA5, SD--PA7
	(Slave mode DEMO board) I2S1: WS--PA4, CK--PA5, SD--PA7
	3. DMA: I2S1 transmission adopts DMA_CH3 channel, I2S1 reception adopts DMA_CH2 channel;
	4. Log printing: slave mode DEMO board PA9(TX), baud rate: 115200

	 /* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. After the master mode DEMO board and the slave mode DEMO board PA4, PA5, PA7 are connected, 
	   the slave mode DEMO board is connected to the serial port printing tool, power on,
       First press and hold the reset button of the master mode DEMO board, then press the reset button of the slave mode DEMO board, 
       and then release the reset button of the master mode DEMO board after the slave mode DEMO board runs to check that the print test is successful;

4. Matters needing attention
	Two demo boards are required, one board to program the master mode program, one board to program the slave mode program,
	the two boards need to be powered on together, and connect the VCC and GND of the two boards.