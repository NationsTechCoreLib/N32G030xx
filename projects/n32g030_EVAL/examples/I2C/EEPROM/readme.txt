1������˵��

    ������չʾ��ͨ��I2Cģ�����ⲿEEPRON��ͨ�š�   

2��ʹ�û���

   �������������
        IDE���ߣ�KEIL MDK-ARM 5.21.1.0
    
    Ӳ��������
        �����壺N32G030C8L7-STB V1.0


3��ʹ��˵��
	
    1����ʱ�ӣ�48MHz
    2��I2C1 ���ã�
            SCL   -->  PB6          
            SDA   -->  PB7         
            CLOCK:400KHz
            
    3��USART1���ã�
            TX  -->  PA9   
            RX  -->  PA10           
            �����ʣ�115200
    
    4������ʹ��EEPROM�ͺ�:
	    AT24C04������4kb��
        

    5�����Բ���������
        a�����EEPROM����
        b���������ش��븴λ����
        c���Ӵ��ڿ���ӡ��Ϣ����֤���

4��ע������
   ��

1. Function description

     This example demonstrates the communication with the external EEPRON through the I2C module.

2. Use environment

    Software development environment:
         IDE tool: KEIL MDK-ARM 5.21.1.0
    
     Hardware environment:
         Development board: N32G030C8L7-STB V1.0


3. Instructions for use

     1. Main clock: 48MHz
     2. I2C1 configuration:
             SCL --> PB6
             SDA --> PB7
             CLOCK: 400KHz
            
     3. USART1 configuration:
             TX --> PA9
             RX --> PA10
             Baud rate: 115200
    
     4. Test using EEPROM model:
            AT24C04 (capacity 4kb)
        

     5. Test steps and phenomena
         a, check the EEPROM connection
         b, compile and download the code, reset and run
         c, view the print information from the serial port and verify the result

4. Matters needing attention
    without