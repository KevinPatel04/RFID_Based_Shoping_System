# RFID_Based_Shoping_System

## Abstract:
In metro cities we can see you a huge rush at shopping malls on holidays and weekends. This becomes even more when there are huge offers and discounts. Nowadays people purchase a variety of items and put them in the trolley. After total purchasing one should approach counter for billing purpose. By using barcode the cashier prepares the bill which is a time consuming process. This results in long queues at the billing counters. This project presents an idea to develop a system in shopping malls to overcome the above problem. To achieve this all products in the mall should be equipped with RFID tags and smart check-out counter. First of all customer must login / signup with the system. When one puts any product on RFID reader its code will be detected automatically, the item name and cost will be displayed on the LCD, thereby the cost gets added to the total bill. You need to continue this process until you complete with scanning of all the products. After completion, you may generate the bill which would be mailed to your registered account and the amount will be debited from your registered credit card. By doing this lot of time and man power can be saved.

## Requirement
#### Softwares:
 WAMP/XAMP/LAMP for MYSQL database <br> Netbeans/IntelIJ for development purpose <br>
 JAVA 1.8 (JDK 1.8 & JRE 1.8)

#### Hardware:
 Arduino UNO (2 piece / 1 piece) <br>RC522 RFID scanner module <br>Buzzer, LED's (2 RED AND 2 GREEN), Jumper Cables, 

## Setup:
 Download the zip file and extract all the folder's from it.

 Keep this extracted folder named "RFID_Based_SmartShoppingSystem" in 'C://' only which     look like "C://RFID_Based_SmartShoppingSystem/" to avoid errors.

 Import the SQL file named "rfid_basedshoppingsystem" to your Database. 

 Attach 2 Arduino boards or one to your system and See the circuit diagram for reference.  

#### Note: Avoid Changing Directory Structure provided to you and follow all setup steps thouroly;  

###  Contains To be Modified Before running:
#### In DBConnection.java
line: 23 -> Enter the servername of your DB in place of "servername",
       Enter the port_number of your DB in place of "port_number",
       Enter User name and Password in place of "User_Name here" & "Password here" respectively
connection = DriverManager.getConnection("jdbc:mysql://servername:port_number/rfid_basedshoppingsystem?useSSL=false", "User_Name here", "Password here");
 
#### In Email.java
line: 114->  Enter sender's email in place of "your_email@gmail.com" in String user = "your_email@gmail.com";

line: 115-> Enter sender's account's password in place of "your password" in String pss = "your password";

line: 154 -> Enter reciever's email in place of "To_email_address"

#### In Email_Bill.java
line: 92 -> Enter sender's email in place of "your_email@gmail.com" in String user = "your_email@gmail.com";

line: 93 -> Enter sender's account's password in place of "your password" in String pss = "your password";

line: 147-> Enter reciever's email in place of "To_email_address" and Pdf file path in place of "C:\\RFID_Based_SmartShoppingSystem\\pdfFiles\\@kevin.pdf" in sendMessage("To_email_address","C:\\RFID_Based_SmartShoppingSystem\\pdfFiles\\@kevin.pdf");
 
#### In Java2arduino.java 
line: 14 -> Check the your COM port of arduino connected to Arduino with LED's and enter here appropriate one in place of "COM4" in Arduino("COM4", 9600);

#### In Arduino2java.java
line: 76 -> Check the your COM port of arduino connected to Arduino with RC522 module and enter here appropriate
    one in place of "COM3" in System.setProperty("gnu.io.rxtx.SerialPorts", "COM3");
    
For Extra Reference Please view "Smart shopping system final.pdf" or "Smart shopping system final.pptm";
-
