1������˵��
    ͨ��PC13��������֡�

2��ʹ�û���

    �������������KEIL MDK-ARM V5.25

        Ӳ��������
        1������������N32G030C8L7-STB V1.0����
        2��MCU��N32G030C8L7

3��ʹ��˵��

    ϵͳ���ã�
        1�RRTCʱ�ӣ�LSI
        2�R���ּ��ڣ�PC13
        3���������ã�
                    - ����ΪUSART1��TX��PA9  RX��PA10��:
                    - ����λ��8
                    - ֹͣλ��1
                    - ��żУ�飺��
                    - �����ʣ� 115200 
    ʹ�÷�����
        1���������¼�������壬�ϵ�󣬸�PC13���������PC13ע��ߵ�ƽ�����ڴ�ӡ���Tamper interrupt��
                
4��ע������
    ��  
    
1. Function description

	1. Tamper is triggered by detecting PC13 IO.

2. Use environment

	Software development environment: KEIL MDK-ARM V5.25
	Hardware environment:
		1. based on the evaluation board N32G030C8L7-STB V1.0 development
		2. MCU: N32G030C8L7

3. Instructions for use

	System configuration:

		1. RTC Clock source: LSI
        2. Tamper detection IO: PC13
		3. Serial port configuration:
							- Serial port: USART1 (TX: PA9 RX: PA10) :
							- Data bit: 8
							- Stop bit: 1
							- Parity check: None
							- Baud rate: 115200

	Instructions:
		1. After compiling, it is burned to the evaluation board. After powering on, connect PC13 to the external pull-up, high level is artificially injected into PC13 and "Tamper interrupt" is output through the serial port. 
        
4. Matters needing attention
	None