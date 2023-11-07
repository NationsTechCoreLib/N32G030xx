1������˵��
    1��TIM3 CH2��������ͨ��CH1�½��غ�CH2�����ؼ���ռ�ձȺ�Ƶ��
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM3 CLK=48M
        2���жϣ�
                    TIM3 CC2�Ƚ��жϴ򿪣����ȼ�1
        3���˿����ã�
                    PA7ѡ��ΪTIM3��CH2����
                    PA3ѡ��ΪIO���
        4��TIM��
                    TIM3 CH1����CH2�źŵ��½��ء�TIM3 CH2����CH2�źŵ�������
    ʹ�÷�����
        1�������򿪵���ģʽ������PA3��PA7����Frequency��DutyCycle��gOnePulsEn��ӵ�watch����
        2���������к�Ĭ��gOnePulsEn=0��ÿ���ֶ���gOnePulsEn=1����ʱ���Կ��������񵽵�ռ�ձȺ�Ƶ�ʵ�ֵ�ֱ�洢��DutyCycle��Frequency����
4��ע������
    ��

1. Function description
    1. TIM3 CH2 capture pin calculates the duty cycle and frequency through the falling edge of CH1 and the rising edge of CH2
2. Use environment
     Software development environment: KEIL MDK-ARM V5.34.0.0
     Hardware environment: Developed based on N32G031C8L7_STB V1.0
3. Instructions for use
     System Configuration;
         1. Clock source:
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM3 CLK=48M
         2. Interrupt:
                    TIM3 CC2 compare interrupt is turned on, priority level 1
         3. Port configuration:
                    PA7 is selected as the CH2 input of TIM3
                    PA3 is selected as IO output
         4. TIM:
                    TIM3 CH1 captures the falling edge of CH2 signals.TIM3 CH2 captures the rising edge of CH2. 
     Instructions:
         1. Open the debug mode after compiling, connect PA3 and PA7, and add the variables TIM3Freq and gOnePulsEn to the watch window
         2. The default gOnePulsEn=0, manually give gOnePulsEn=1 each time, then you can see that the values of the duty cycle and frequency captured are stored in the DutyCycle and Frequency variables.
4. Matters needing attention
    None