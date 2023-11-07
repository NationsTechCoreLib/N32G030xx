1������˵��

    �ò�����ʾ��LPUART���ͨ����PC��ͨ�Ż���STOPģʽ��
    MCU����STOPģʽ������PC������ȷ�����ݻ���MCU����ʶ����ȷ�Ļ����¼�
ʱ��WUF�жϽ�����������MCU��
    Ϊ��ȷ���Ƿ��ѣ�MCU������ȷ����Ϣ��PC������PC����Ƿ���Ԥ�ڵ���Ϣ��
    ���̽��ظ�4�ν��У�����֤��ͬ�Ļ����¼���
    1 ��ʼλ��⣬�緢�ͻ������ݡ�5A��(Hex)
    2 ���ջ������ǿռ�⣬�緢�ͻ������ݡ�5A��(Hex)
    3 һ�������õĽ����ֽڣ��緢�ͻ������ݡ�5A��(Hex)
    4 һ���ɱ�̵�4�ֽ�֡���緢�ͻ������ݡ�4B3C2D1E��(Hex)
    

2��ʹ�û���

    �������������KEIL MDK-ARM Professional Version 5.26.2.0

    Ӳ����������Сϵͳ��N32G030C8L7-STB V1.0


3��ʹ��˵��
	
    ϵͳʱ���������£�
    - ʱ��Դ = HSI + PLL
    - ϵͳʱ�� = 48MHz
    
    LPUART�������£�
    - ������ = 9600 baud
    - �ֳ� = 8����λ���̶���
    - 1ֹͣλ���̶���
    - У����ƽ���
    - Ӳ�������ƽ��ã�RTS��CTS�źţ�
    - �������ͷ�����ʹ��
    
    
    LPUART�����������£�    
    - LPUART_Tx.PA1   
    - LPUART_Rx.PA0     

    
    ���Բ���������
    - Demo��KEIL�����±����������MCU
    - ��λ���У��鿴���ڴ�ӡ��Ϣ��ͨ�����ڷ�����Ӧ���ַ�������MCU���ٴ�
      �鿴���ڴ�ӡ��Ϣ����ʾ�����ѡ������ò������ظ�4��


4��ע������

1. Function description

    This test example demonstrates how LPUART wakes up STOP mode through communication with PC.
     The MCU enters the STOP mode, and the PC sends the correct data to wake up the MCU. When the correct wake-up event is recognized, the WUF interrupt will trigger and wake up the MCU.
     In order to confirm whether to wake up, the MCU will send a confirmation message to the PC, and the PC will check whether it is the expected message.
     The process will be repeated 4 times to verify different wake-up events:
     1 Start bit detection, such as sending wake-up data ��5A�� (Hex)
     2 The receiving buffer is not empty detection, such as sending wake-up data ��5A�� (Hex)
     3 One configurable receive byte, such as sending wake-up data ��5A�� (Hex)
     4 One programmable 4-byte frame, such as sending wake-up data ��4B3C2D1E�� (Hex)
    

2. Use environment

    Software development environment: KEIL MDK-ARM Professional Version 5.26.2.0

    Hardware environment: minimum system board N32G030C8L7-STB V1.0


3. Instructions for use

    The system clock configuration is as follows:
    -Clock source = HSI + PLL
    -System clock = 48MHz
    
    The LPUART configuration is as follows:
    -Baud rate = 9600 baud
    -Word length = 8 data bits (fixed)
    -1 stop bit (fixed)
    -Verification control disabled
    -Hardware flow control disabled (RTS and CTS signals)
    -Receiver and transmitter enable
    
    
    The LPUART pin connections are as follows:
    -LPUART_Tx.PA1
    -LPUART_Rx.PA0

    
    Test steps and phenomena:
    -After the Demo is compiled in the KEIL environment, download it to the MCU
    -Reset operation, check the serial port print information, send the corresponding character through the serial port, wake up the MCU, and again
      Check the serial port print information (prompt "wake up"), this step needs to be repeated 4 times


4. Matters needing attention