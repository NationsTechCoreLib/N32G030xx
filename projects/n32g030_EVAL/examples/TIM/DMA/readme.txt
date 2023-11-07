1������˵��
    1��TIM1 CH3 CH3N�����ź�ÿ6�����ڸı�һ��ռ�ձ�
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM1 CLK=48M,DMA CLK=48M
        2���˿����ã�
                    PA10ѡ��ΪTIM1 CH3���
                    PB15ѡ��ΪTIM1 CH3N���
        3��TIM��
                    TIM1 CH3 CH3N���������ÿ6�����ڴ���һ��DMA����
        4��DMA��
                DMA1_CH5ͨ��ѭ����ģʽ����3������SRC_Buffer[3]������TIM1 CCDAT3�Ĵ���
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�TIM1 CH3 CH3N�Ĳ���
        2��TIM1��6�����ڸı�һ��CH3 CH3N��ռ�ձȣ�ѭ���ı�
4��ע������
    ��

1. Functional description
    1. TIM1 CH3 CH3N complementary signal changes duty cycle every 6 cycles
2. Use environment
    Software development environment: KEIL MDK-ARM V5.34.0.0
    Hardware environment: Developed based on the evaluation board N32G031C8L7-STB V1.0
3. Instructions for Use
    System configuration:
        1. Clock source:
            HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, TIM1 CLK=48M, DMA CLK=48M
        2. Port configuration:
            PA10 selected as TIM1 CH3 Output
            PB15 selected as TIM1 CH3N Output
        3. TIM:
            TIM1 CH3 CH3N complementary output triggers DMA transmission every 6 cycles
        4. DMA:
            DMA1_ CH5 Channel circular mode handling 3 half-Word SRC_ Buffer[3] variable to TIM1 CCDAT3 register
     Instructions:
         1. After compiling, turn on the debug mode, use an oscilloscope or logic analyzer to observe the waveform of TIM1 CH3 CH3N
         2. Change the duty cycle of CH3 and CH3N once in 6 cycles of TIM1, and change cyclically
4. Matters needing attention
    None