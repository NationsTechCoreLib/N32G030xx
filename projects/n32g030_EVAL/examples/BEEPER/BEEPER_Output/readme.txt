1. ����˵��
    ������չʾ������ģ����÷�

2. ʹ�û���
    �����������: KEIL MDK-ARM 5.26
    Ӳ��������     N32G030C8L7-STB V1.0

3. ʹ��˵��
    �������ģ�����÷���������:ʱ�ӣ�I/O�� 
         1. ʱ��Դ��HSE+PLL
         2. ��ʱ�ӣ�48MHz
         3. GPIO��PA6--AF_PP, PA7--AF_PP

    ����Demo�Ĳ��Բ�������� 
         1. ��������س���λ����
         2. ��ʾ�����鿴���Σ���֤���

4. ע������
    1��PA6��PA7�Ĳ��λ���
    2����������3603-1A���������̣���Ӧ�������������������������ģ��Ĵ�����һ������ע��ʹ�õ�ǰ���µ�pack����1.0.1�汾�����ϣ�
    3��֧�ֽ���LPRUNģʽ����ʱ���Ƶ��Ϊpclk1��4��Ƶֵ
    4��APBʱ��Ƶ��ѡ��Ĵ���λ��freq_sel����ֵ������Ƶ��������������β�����ʧ���Ч��

1. Function description
    This routine shows the use of the beeper module

2. Use environment
    Software environment:  KEIL MDK-ARM 5.26
    Hardware environment: N32G030C8L7-STB V1.0

3. Instructions for use
    Describe the configuration method of related modules; for example: clock, I/O, etc. 
        1. Clock source: HSE+PLL
        2. Main clock: 48MHz
        3. GPIO: PA6--AF_PP, PA7--AF_PP
                  
    Describe the test steps and phenomena of Demo 
        1. After compiling, download the program to reset and run;
        2. Use oscilloscope to view the waveform and verify the result
 
4. Matters needing attention
    1. Waveforms of PA6 and PA7 are complementary
    2. This routine is 3603-1A beeper routine, the corresponding driver, project and other changes (register is not the same), pay attention to the use of the current latest pack pack (version 1.0.1 and above)
    3. Support to enter the LPRUN mode, at this time the output frequency is pCLK1 4 division value
    4. The value of APB clock frequency selection register bit (freq_SEL) is determined according to the main frequency, so that the output waveform will not be distorted