1������˵��
    1��ͨ���趨����ʱ�䴥���жϡ�
    2��ͨ�����ѱ�־λ������IO���


2��ʹ�û���

    �������������KEIL MDK-ARM V5.25

    Ӳ��������
    1������������N32G030C8L7-STB V1.0����
    2��MCU��N32G030C8L7


3��ʹ��˵��

    ϵͳ���ã�
        1�������Ի���ʱ��Դ��RTCCLK��1HZ��
        2���������ã�
                    - ����ΪUSART1��TX��PA9  RX��PA10��:
                    - ����λ��8
                    - ֹͣλ��1
                    - ��żУ�飺��
                    - �����ʣ� 115200 


    ʹ�÷�����
        1���������¼�������壬�ϵ�󣬴���ÿ��4s���ӡI am in rtc_wkup��
            
4��ע������
    ��
    
 
1. Function description

	1. Trigger interrupt by setting wake up time
	2. Configure IO output by wake up flag bit

2. Use environment

	Software development environment: KEIL MDK-ARM V5.25
	Hardware environment:
		1. based on the evaluation board N32G030C8L7-STB V1.0 development
		2. MCU: N32G030C8L7

3. Instructions for use

	System configuration:

		1. periodic wake up clock source: RTCCLK (1HZ)
		2. Serial port configuration:

							- Serial port: USART1 (TX: PA9 RX: PA10) :
							- Data bit: 8
							- Stop bit: 1
							- Parity check: None
							- Baud rate: 115200

	Instructions:
		1. After compilation, it is burned to the evaluation board. After power-on, the serial port will print "I am in rtc_wkup" every 4s

4. Matters needing attention
	None