1������˵��
    1��TIM1 һ�����ں�ͬʱ�ı����ں�ռ�ձ�
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.30.0.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,TIM1 CLK=48M,DMA CLK=48M
        2���˿����ã�
                    PA8ѡ��ΪTIM1 CH1���
        3��TIM��
                    TIM1 CH1 ��������ڴ���DMA burst���䣬����AR,REPCNT,CCDAT1�Ĵ������ı�ռ�ձȺ����ں��ظ�������
        4��DMA��
                    DMA1_CH5ͨ������ģʽ����3������SRC_Buffer[3]������TIM1 DMA�Ĵ���
    ʹ�÷�����
        1�������򿪵���ģʽ����ʾ���������߼������ǹ۲�TIM1 CH1�Ĳ���
        2��TIM1�ĵ�һ�����ڽ����󣬺���Ĳ���ΪDMA���˵ĸı����ں�ռ�ձȵĲ���
4��ע������
    ��

1. Function description
     1. TIM1 changes the period and duty cycle at the same time after one cycle
2. Use environment
    Software development environment: KEIL MDK-ARM V5.34.0.0
    Hardware environment: Developed based on the evaluation board N32G031C8L7-STB V1.0
3. Instructions for use
    System Configuration:
        1. Clock source:
                     HSE=8M, PLL=48M, AHB=48M, APB1=48M, APB2=48M, TIM1 CLK=48M, DMA CLK=48M
        2. Port configuration:
                     PA8 is selected as TIM1 CH1 output
        3. TIM:
            TIM1 CH1 output, periodically triggered DMA burst transmission, loading AR, REPCNT, CCDAT1 registers, changing duty cycle, period and repeat counter
        4. DMA:
                     The DMA1_CH5 channel in normal mode transfers 3 half-word SRC_Buffer[3] variables to the TIM1 DMA register
    Instructions:
        1. Open debugging mode after compilation and observe TIM1 CH 1 waveform with oscilloscope or logic analyzer
         2. After the first cycle of TIM1 is over, the following waveforms are the waveforms of changing cycle and duty cycle of DMA transport
4. Matters needing attention
    None