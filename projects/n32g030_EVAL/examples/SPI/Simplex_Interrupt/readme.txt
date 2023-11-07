1������˵��

	1��SPI �����жϷ��ͺͽ�������

2��ʹ�û���

	/* ���������������ǰ����ʹ�õ�����������Ƽ��汾�� */
	IDE���ߣ�KEIL MDK-ARM 5.30.0.0
	SDK�汾��Nationstech.N32G030_Library.0.1.0

	/* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
	�����壺N32G030CL-STB V1.0 V1.0

3��ʹ��˵��
	
	/* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
	1��SystemClock��108MHz
	2��GPIO��SPI1: SCK--PA5�� MOSI--PA7,
	                SPI2: SCK--PB13��MISO--PB14
	3���жϣ�SPI1 �ж���ں��� SPI1_IRQHandler��SPI2 �ж���ں��� SPI2_IRQHandler

	/* ����Demo�Ĳ��Բ�������� */
	1.��������س���λ���У�
	2.SPI1 ��������Ҫ����ʱ���� SPI1_IRQHandler �жϺ������ͣ�SPI2 ��������Ҫ����ʱ���� SPI2_3_IRQHandler�жϺ������գ����ݴ�����ɺ󣬲鿴 TransferStatus ״̬Ϊ PASSED��

4��ע������
	�����ߡ������������豸��ΪMOSI���ţ��ڴ��豸��ΪMISO����



1. Function description

	1. SPI single-wire interrupt sending and receiving data

2. Use environment

	/* Software development environment: the name and version number of the software tool used in the current project */
	IDE tool: KEIL MDK-ARM 5.30.0.0
	SDK version: Nationstech.N32G030_Library.0.1.0

	/* Hardware environment: the development hardware platform corresponding to the project */
	Development board: N32G030CL-STB V1.0 V1.0

3. Instructions for use

	/* Describe related module configuration methods; for example: clock, I/O, etc. */
	1. SystemClock: 108MHz
	2. GPIO: SPI1: SCK--PA5, MOSI--PA7,
	SPI2: SCK--PB13, MISO--PB14
	3. Interrupt: SPI1 interrupt entry function SPI1_IRQHandler, SPI2 interrupt entry function SPI2_IRQHandler

	/* Describe the test steps and phenomena of the Demo */
	1. After compiling, download the program to reset and run;
	2. Enter the SPI1_IRQHandler interrupt function to send when SPI1 has data to send, 
	   and enter the SPI2_3_IRQHandler interrupt function to receive when SPI2 has data to receive. 
	   After the data transmission is completed, check the TransferStatus status as PASSED;

4. Matters needing attention
	The "single wire" data lines are MOSI pins on the master side and MISO pins on the slave side.