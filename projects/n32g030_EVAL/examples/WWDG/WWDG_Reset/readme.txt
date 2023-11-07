1������˵��
	1��WWDG��λ���ܡ�


2��ʹ�û���

	�������������KEIL MDK-ARM V5.25

    Ӳ��������
		1������������N32G030CL-STB V1.0����
		2��MCU��N32G030C8


3��ʹ��˵��
	
	ϵͳ���ã�
		1��WWDGʱ��Դ��PCLK1
		2������ֵ��31.96ms < n <43.52ms
                3��ָʾ�ƣ�PA4(LED1)   PA5(LED2)
             
	���Բ���������
		1����KEIL�±������¼�������壬�ϵ��ָʾ��LED2��ͣ����˸��˵������ֵˢ�������������������С�
                2������Delay(38)���������ĳ�С��32���ߴ���44ʱ������ϵͳ��һֱ���ڸ�λ״̬��LED1����


4��ע������
	1��������ֵ��Сʱ��ϵͳ����Ƶ���ĸ�λ״̬����ʱ��������������޷��������ء����������ڿ���WWDGǰ����1����ʱ������������󡣵�ȻҲ���Բ�����ʱ��ֱ�ӽ�BOOT0�������߼����������ء� 

	

1. Function description

    WWDG reset function.
    

2. Use environment

    Software development environment:
       IDE tool: KEIL MDK-ARM 5.25
    
    Hardware environment:
       1. Development Board N32G030CL-STB V1.0
	   2. MCU��N32G030C8


3. Instructions for use

    System Configuration:
       1. IWDG clock source: PCLK1
	   2. Window value: 31.96ms < n <43.52ms
       3. light Indicator: PA4(LED1)   PA5(LED2)

    Test steps and phenomenon��
       1. Compile and download the code to reset and run, the indicator LED2 keeps flashing. 
	      It means that the window value is refreshed normally and the code is running normally.
       2. When the parameter of the Delay() function is changed from 38 to less than 32 or greater than 44, 
	      the entire system will always be in the reset state. LED1 is on.

		
4. Matters needing attention
    1. When the window value is very small, the system is in a frequent reset state, and at this time, it is easy to 
	   cause the program to fail to download normally. In this routine, 1s delay is added before WWDG is 
	   turned on to avoid this phenomenon. Of course, without delay, you can directly pull up the BOOT0 pin to download normally.