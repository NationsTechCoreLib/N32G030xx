1������˵��
    1��HDIVִ��һ�γ�����������ж�����ͨ�����ڷ����̺�����
2��ʹ�û���
    �������������  KEIL MDK-ARM V5.26.2.0
    Ӳ��������      ����N32G030C8L7-STB V1.0����
3��ʹ��˵��
    ϵͳ���ã�
        1��ʱ��Դ��
                    HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,HDIV CLK=48M
        2���˿����ã�
                            PA9ѡ��Ϊ�������
                    PA10ѡ��Ϊ��������
        3��HDIV��
                    HIDV�жϴ����ȼ�0������ 0x1E240���� 0x7B�Ľ��
    ʹ�÷�����
        1�������򿪵���ģʽ��������HDIV�ļĴ�����
        2������ִ�к󣬿��Կ����̵Ľ��Ϊ1003�������Ľ��Ϊ87��ͬʱ����Ҳ���ӡ�����Ϣ
4��ע������
    ��

1. Function description
     1. HDIV performs a division, and sends the quotient and remainder through the serial port in the completion interrupt
2. Use environment
     Software development environment: KEIL MDK-ARM V5.26.2.0
     Hardware Environment: Developed based on N32G030C8L7-STB V1.0
3. Instructions for use
     System Configuration;
         1. Clock source:
                     HSE=8M,PLL=48M,AHB=48M,APB1=48M,APB2=48M,HDIV CLK=48M
         2. Port configuration:
                             PA9 is selected as serial output
                     PA10 is selected as serial input
         3. HDIV:
                     HIDV interrupt on priority 0, calculate the result of dividing 0x1E240 by 0x7B
     Instructions:
         1. Open the debug mode after compiling, and open the register of the variable HDIV
         2. After the program is executed, you can see that the result of the quotient is 1003, the result of the remainder is 87, and the serial port will also print relevant information
4. Matters needing attention
     none