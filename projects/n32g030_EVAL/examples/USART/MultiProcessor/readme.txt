1������˵��

    �ò�����ʾ�����ʹ��USART�ദ����ģʽ��USARTy��USARTz������USART1
��USART2��
    ���ȣ��ֱ�����USARTy��USARTz�ĵ�ַΪ0x1��0x2��USARTy������USARTz
�����ַ�0x33��USARTz�յ�0x33���㷭תLED1��LED2��LED3�����š�
    һ��KEY1_INT_EXTI_LINE�߼�⵽�����أ������EXTI0�жϣ���
EXTI0_IRQHandler�жϴ�������(the ControlFlag = 0)��USARTz���뾲Ĭ
ģʽ���ھ�Ĭģʽ�У�LED����ֹͣ��ת��ֱ��KEY1_INT_EXTI_LINE�߼�⵽
������(the ControlFlag = 1)����EXTI0_IRQHandler�жϴ������У�USARTy
���͵�ַ0x102����USARTz��LED��������������ת��


2��ʹ�û���

    �������������KEIL MDK-ARM Professional Version 5.26.2.0

    Ӳ����������Сϵͳ��N32G030C8L7-STB V1.0


3��ʹ��˵��
	
    ϵͳʱ���������£�
    - ʱ��Դ = HSI + PLL
    - ϵͳʱ�� = 48MHz
    
    USARTy�������£�
    - ������ = 115200 baud
    - �ֳ� = 9����λ
    - 1ֹͣλ
    - У����ƽ���
    - Ӳ�������ƽ��ã�RTS��CTS�źţ�
    - �������ͷ�����ʹ��  
    
    
    USART�����������£�    
    - USART1_Tx.PA9     <------->  USART2_Rx.PA3
    - USART1_Rx.PA10   <------->   USART2_Tx.PA2    
    
    KEY1_INT_EXTI_LINE.PA6    <------->   KEY3
    
    LED1    <------->   PB1
    LED2    <------->   PB6
    LED3    <------->   PB7

    
    ���Բ���������
    - Demo��KEIL�����±����������MCU
    - ��λ���У��۲�LED1~3�Ƿ�����˸״̬
    - ������KEY���۲�LED1~3�Ƿ�ֹͣ��˸
    - �ٴΰ�����KEY���۲�LED1~3�Ƿ�ָ���˸


4��ע������


1. Function description

    This test example demonstrates how to use the USART multiprocessor mode. USARTy and USARTz can be USART1 and USART2.
    First, set the addresses of USARTy and USARTz to 0x1 and 0x2 respectively. USARTy continuously sends the character 0x33 to 
USARTz. USARTz receives 0x33 and flips the pins of LED1, LED2, and LED3.
    Once the KEY1_INT_EXTI_LINE line detects the rising edge, the EXTI0 interrupt is generated. In the EXTI0_IRQHandler interrupt 
processing function (the ControlFlag = 0), the USARTz enters the silent mode. In the silent mode, the LED pin stops toggling until 
the KEY1_INT_EXTI_LINE line detects the rising edge ( the ControlFlag = 1). In the EXTI0_IRQHandler interrupt processing function, 
USARTy sends address 0x102 to wake up USARTz. The LED pin restarts toggling.


2. Use environment

    Software development environment: KEIL MDK-ARM Professional Version 5.26.2.0

    Hardware environment: minimum system board N32G030C8L7-STB V1.0


3. Instructions for use

    The system clock configuration is as follows:
    -Clock source = HSI + PLL
    -System clock = 48MHz
    
    The USARTy configuration is as follows:
    -Baud rate = 115200 baud
    -Word length = 9 data bits
    -1 stop bit
    -Verification control disabled
    -Hardware flow control disabled (RTS and CTS signals)
    -Receiver and transmitter enable
    
    
    The USART pin connections are as follows:
    -USART1_Tx.PA9 <-------> USART2_Rx.PA3
    -USART1_Rx.PA10 <-------> USART2_Tx.PA2
    
    KEY1_INT_EXTI_LINE.PA6 <-------> KEY3
    
    LED1 <-------> PB1
    LED2 <-------> PB6
    LED3 <-------> PB7

    
    Test steps and phenomena:
    -After the Demo is compiled in the KEIL environment, download it to the MCU
    -Reset operation, observe whether LED1~3 are blinking
    -Press the KEY button and observe if LED1~3 stop flashing
    -Press the KEY button again and observe whether LED1~3 resume flashing


4. Matters needing attention