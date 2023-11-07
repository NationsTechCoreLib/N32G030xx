1������˵��

	1��SPI ����д������ W25Q128

2��ʹ�û���

	/* ���������������ǰ����ʹ�õ�����������Ƽ��汾�� */
	IDE���ߣ�KEIL MDK-ARM 5.30.0.0
	SDK�汾��Nationstech.N32G030_Library.0.1.0

	/* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
	�����壺N32G030CL-STB V1.0 V1.0

3��ʹ��˵��
	
	/* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
	1��SystemClock��48MHz
	2��SPI1: NSS--PA4��SCK--PA5��MISO--PA6��MOSI--PA7

	/* ����Demo�Ĳ��Բ�������� */
	1����������س���λ���У�
	2��ͨ�� SPI1 ��ȡ W25Q128 �� ID��Ȼ��д���ݣ��ٶ��������Ƚ϶�д���ݣ��鿴 TransferStatus1 ״̬Ϊ PASSED��Ȼ������飬��������������

4��ע������
	�� N32G030CL-STB V1.0 V1.0 �������ϵ� SPI1 �ӿڽ��� N32G457QE_EVB ������� W25Q128 �ϣ�������������Ҫ���ء�




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