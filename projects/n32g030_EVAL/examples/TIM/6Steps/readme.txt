1������˵��
    1��systick 100ms����TIM1���6�����ನ��
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ����:
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM1 CLK=48M
        2���жϣ�
                    TIM1 COM�¼��жϴ򿪣����ȼ�1
                    Systick 100ms�жϣ����ȼ�0
        3���˿����ã�
                    PA8ѡ��ΪTIM1 CH1���
                    PA9ѡ��ΪTIM1 CH2���
                    PA10ѡ��ΪTIM1 CH3���
                    PB13ѡ��ΪTIM1 CH1N���
                    PB14ѡ��ΪTIM1 CH2N���
                    PB15ѡ��ΪTIM1 CH3N���
                    PB12ѡ��ΪTIM1 Breakin����
        4��TIM��
                    TIM1 6·�����������ģʽ����ɲ������COM�ж�
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�TIM1���������
        2��ÿ��100ms systick����COM�жϣ���TIM��COM�ж��������AB AC BC BA CA CB��6�����ನ��
4��ע������
       ������Ĭ��PA9��PA10��ñ�ӵ�NSLINK�����⴮�ڣ���������PA9��PA10�������ڣ�����������;����ε�������ñ��

1. Function description
    1. systick triggers TIM1 for 100ms to output 6-step commutation waveform
2. Use environment
    Software development environment: KEIL MDK-ARM V5.34.0.0
    Hardware environment: Developed based on the evaluation board N32G031C8L7-STB V1.0
3. Instructions for use
    System Configuration;
        1. Clock source:
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM1 CLK=48M
        2. Interrupt:
                    TIM1 COM event interrupt on, priority 1
                    Systick 100ms interrupt, priority 0
        3. Port configuration:
                    PA8 is selected as TIM1 CH1 output
                    PA9 is selected as TIM1 CH2 output
                    PA10 is selected as TIM1 CH3 output
                    PB13 is selected as TIM1 CH1N output
                    PB14 is selected as TIM1 CH2N output
                    PB15 is selected as TIM1 CH3N output
                    PB12 is selected as TIM1 Breakin input
        4. TIM:
                    TIM1 6-channel complementary freeze output mode, no brake, open COM interrupt
    Instructions:
        1. Open the debug mode after compiling, and observe the output waveform of TIM1 with an oscilloscope or logic analyzer
        2. The systick triggers the COM interrupt every 100ms, and outputs the 6-step commutation waveform of AB AC BC BA CA CB in the COM interrupt of the TIM
4. Matters needing attention
       By default, the PA9 and PA10 jumper caps of the development board are connected to the virtual serial port of NSLINK. If PA9 and PA10 are not used as serial ports in the project, and are used for other purposes, the serial port jumper caps must be unplugged.

