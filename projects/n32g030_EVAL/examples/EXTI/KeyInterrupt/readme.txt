1������˵��

    ������չʾͨ���ⲿ�����жϣ����� LED ��˸


2��ʹ�û���

    /* ���������������ǰ����ʹ�õ�����������Ƽ��汾�� */
    IDE���ߣ�KEIL MDK-ARM 5.21.1.0
      
    /* Ӳ�����������̶�Ӧ�Ŀ���Ӳ��ƽ̨ */
    �����壺N32G030CL-STB V1.0     

3��ʹ��˵��

    /* �������ģ�����÷���������:ʱ�ӣ�I/O�� */
    SystemClock��48MHz
    GPIO��PA5 ѡ����Ϊ�ⲿ�ж���ڣ�PB7 ���� LED(PD3) ��˸


    /* ����Demo�Ĳ��Բ�������� */
    1.��������س���λ���У�
    2.�����ɿ� KEY2 ������LED ��˸��


4��ע������
    ��

1. Function description

    This example shows how to control LED blinking by externally triggering an interrupt.
    

2. Use environment
    Software development environment:  //the name and version number of the software tool used in the current project.
        IDE tool: KEIL MDK-ARM 5.21.1.0
    
    Hardware environment:  //The development hardware platform corresponding to the project.
        Development Board: N32G030CL-STB V1.0


3. Instructions for use

     //Describe related module configuration methods; for example, clock, I/O, etc.
     1. SystemClock: 48MHz
     2. GPIO��PA5 is selected as the external interrupt entry, PB7 controls the LED (PD3) to flash.

     //Describe the test steps and phenomena of the Demo
     1. Compile and download the code to reset and run.
     2. Press and release the KEY2 button,then the LED will flash.

4. Matters needing attention
     None