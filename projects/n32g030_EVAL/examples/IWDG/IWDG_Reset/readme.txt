1������˵��
	IWDG��λ���ܡ�


2��ʹ�û���

	�������������KEIL MDK-ARM V5.25

    Ӳ��������
		1������������N32G030CL-STB V1.0����
		2��MCU��N32G030C8L7


3��ʹ��˵��
	
	ϵͳ���ã�
		1��IWDGʱ��Դ��LSI/128
		2����ʱʱ��ֵ��260ms(4.27ms*61)
                3��ָʾ�ƣ�LED1(PA4) LED2(PA5)
            



	���Բ��輰����
	    1����KEIL�±������¼�������壬�ϵ��ָʾ��LED2��ͣ����˸��˵��IWDG����ι���������������С�
        2����Delay(250)���������ĳ�261���ϣ�����ϵͳ��һֱ���ڸ�λ״̬��LED1����


4��ע������
	1�����ͨ����¼�����棬��Ҫ����DBG_ConfigPeriph(DBG_IWDG_STOP,ENABLE);
	2��260ms�����ۼ���õ��ĳ�ʱʱ��ֵ��ʵ������£�LSIʱ�Ӵ���ƫ�����ʱ�����Ĳ�����ʵ�ʶ�����LSIʱ�ӵ�ƫ�Χ��������ֲᡣ

1. Function description

    IWDG reset function.
    

2. Use environment

    Software development environment:
       IDE tool: KEIL MDK-ARM 5.25
    
    Hardware environment:
       1. Development Board N32G030CL-STB V1.0
	   2. MCU��N32G030C8L7


3. Instructions for use

    System Configuration:
       1. IWDG clock source: LSI/128
	   2. Timeout value: 260ms (4.27ms*61)
       3. light Indicator: LED1(PA4) LED2(PA5)

    Test steps and phenomenon��
       1. Compile and download the code to reset and run.The indicator LED2 
		  keeps flashing. It means that IWDG feeds the dog normally and the code runs normally.
       2. Change the parameter of the Delay() function from 250 to 261 or more, the whole system
          will always be in the reset state, and LED1 will be on.

		
4. Matters needing attention
    1. If you simulate through the programmer, you need to enable DBG_ConfigPeriph(DBG_IWDG_STOP,ENABLE).
	2. 260ms is the timeout value obtained by theoretical calculation. In practice, the LSI clock has deviation, 
	   so the parameters of the delay function are determined according to the actual situation.The skew range of
	   the LSI clock is detailed in the data sheet.