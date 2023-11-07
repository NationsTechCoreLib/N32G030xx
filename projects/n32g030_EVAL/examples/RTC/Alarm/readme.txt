1������˵��
    1��ͨ���趨����ʱ�������������жϡ�
    2��ͨ�����ӱ�־λ������IO���

2��ʹ�û���

    �������������KEIL MDK-ARM V5.25
    Ӳ��������
        1������������N32G030C8L7-STB V1.0����
        2��MCU��N32G030C8L7

3��ʹ��˵��

    ϵͳ���ã�
        1��RTCʱ��Դ��LSI
        2���������ã�
                - ����ΪUSART1��TX��PA9  RX��PA10��:
                - ����λ��8
                - ֹͣλ��1
                - ��żУ�飺��
                - �����ʣ� 115200 
    ʹ�÷�����
        �������¼�������壬�ϵ磬���ڰ��������趨ʱ����д�ӡ�����

4��ע������
    ��
    
1. Function description

	1. Trigger the alarm interrupt by setting the alarm time.
	2. Configure I/O output through the alarm flag

2. Use environment

	Software development environment: KEIL MDK-ARM V5.25
	Hardware environment:
		1. based on the evaluation board N32G030C8L7-STB V1.0 development
		2. MCU: N32G030C8L7

3. Instructions for use

	System configuration:

		1. RTC clock source: LSI
		2. Serial port configuration:
							- Serial port: USART1 (TX: PA9 RX: PA10) :
							- Data bit: 8
							- Stop bit: 1
							- Parity check: None
							- Baud rate: 115200

	Instructions:
		After compiling, it is burned to the evaluation board, powered on, and the serial port prints the output according to the time set by the alarm clock.

4. Matters needing attention
	None