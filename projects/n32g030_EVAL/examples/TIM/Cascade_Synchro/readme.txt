1������˵��
    1��TIM1�����ſ�TIM3
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ����:
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM1 CLK=48M,TIM3 CLK=48M
        2���˿����ã�
                    PA8ѡ��ΪTIM1 CH1���
                    PA4ѡ��ΪTIM3 CH1���
        3��TIM��
                    TIM1 �������ſ�TIM3
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�TIM1 CH1��TIM3 CH1����
        2��TIM3 4��������TIM1
4��ע������
    ��

1. Function description
     1. TIM1 cycle gated TIM3
2. Use environment
    Software development environment: KEIL MDK-ARM V5.34.0.0
    Hardware environment: Developed based on the evaluation board N32G031C8L7-STB V1.0
3. Instructions for Use
    System configuration;
        1. Clock source:
            HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, TIM1 CLK=48M, TIM3 CLK=48M
        2. Port configuration:
                     PA8 is selected as TIM1 CH1 output
                     PA4 is selected as TIM3 CH1 output
        3. TIM:
                     TIM1 cycle gating TIM3
    Instructions:
        1. Open debugging mode after compilation and observe TIM1 CH1, TIM3 CH1 waveforms with an oscilloscope or logic analyzer
         2. TIM3 4 times cycle TIM1
4. Matters needing attention
    None