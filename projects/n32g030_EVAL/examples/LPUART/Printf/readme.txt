1������˵��

    �ò�����ʾ��LPUART��PC��ͨ����ѯ����ʶʵ�ֵĻ���ͨ�š�
    �ض���printf������LPUART����ʹ��printf���������Ϣ���նˡ�


2��ʹ�û���

     �������������KEIL MDK-ARM Professional Version 5.26.2.0

     Ӳ����������Сϵͳ��N32G030C8L7-STB V1.0


3��ʹ��˵��
	
    ϵͳʱ���������£�
    - ʱ��Դ = HSI + PLL
    - ϵͳʱ�� = 48MHz
    
    LPUART�������£�
    - ������ = 115200 baud
    - �ֳ� = 8����λ���̶���
    - 1ֹͣλ���̶���
    - У����ƽ���
    - Ӳ�������ƽ��ã�RTS��CTS�źţ�
    - �������ͷ�����ʹ��
    
    LPUART�����������£�
    - LPUART_Tx.PA1 
    
    ���Բ���������
    - Demo��KEIL�����±����������MCU
    - ��λ���У��鿴���ڴ�ӡ��Ϣ


4��ע������

1. Function description

     This test example demonstrates the basic communication between LPUART and PC by querying the detection mark.
     Redirect the printf function to LPUART, and use the printf function to output messages to the terminal.


2. Use environment

      Software development environment: KEIL MDK-ARM Professional Version 5.26.2.0

      Hardware environment: minimum system board N32G030C8L7-STB V1.0


3. Instructions for use

     The system clock configuration is as follows:
     -Clock source = HSI + PLL
     -System clock = 48MHz
    
     The LPUART configuration is as follows:
     -Baud rate = 115200 baud
     -Word length = 8 data bits (fixed)
     -1 stop bit (fixed)
     -Verification control disabled
     -Hardware flow control disabled (RTS and CTS signals)
     -Receiver and transmitter enable
    
     The LPUART pin connections are as follows:
     -LPUART_Tx.PA1
    
     Test steps and phenomena:
     -After the Demo is compiled in the KEIL environment, download it to the MCU
     -Reset operation, view serial port print information


4. Matters needing attention