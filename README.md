# ESP32-WiFi-AP-Cookbook

ตัวอย่างที่นำมาใช้คือ การสร้าง WiFi-AP นำมาจาก Project ST2567_ESP32_ESP-IDF_WiFi-AP 


ส่วนของการแก้ไข ทำการแก้ไขใน Kconfig.projbuild เพื่อตั้งค่า ที่อยู่ WiFi ทำการเพิ่มการ Run ข้อความเมื่อสามารถเชื่อม WiFi สำเร็จ จะขึ้นข้อความที่อยู่และรหัสของ WiFi ขึ้นมา


### ขั้นตอนการทำ project

#### 1.สร้าง Espressif IDF project ใหม่

1.เลือกตัวอย่างโปรเจค โดยการคลิกเลือก ESP-ISF

![image](https://github.com/user-attachments/assets/3b2166b0-ffe2-4e03-af78-66003eb544e4)



ค้นหาเทมเพลต พิมพ์ softAP

2.เลือก softAP

3.กด Yes เมื่อมีการแจ้งเตือนแสดงขึ้นมา



![image](https://github.com/user-attachments/assets/e8b9a767-1155-4184-912f-7bca1b104810)


4.ยืนยันว่าเลือกรุ่นของ idf เป็น V5.3 ขึ้นไป



#### 2. แก้ไขไฟล์ config

1 . เปิดไฟล์ Kconfig.projbuild ในโฟลเดอร์ main ด้วย text editor


![image](https://github.com/user-attachments/assets/17f2ac6e-945e-4eb1-89db-cf35ef55ad15)

  เปิด Kconfig.projbuild

เปลี่ยนชื่อของ wifi ssid

เปลี่ยน password

ทั้งชื่อและ password จะใช้ตอนค้นหาและเชื่อมกับ access point โดยตั้งเป็นของตนเอง


2. ใช้ Laptop หรือ Smartphone ค้นหา Accesspoint


![462643697_1269717570704033_4292127068604543875_n](https://github.com/user-attachments/assets/4e3c42f9-a274-40d4-b1c5-357f965bbd64)


เจอ "SSID" ในรายการ Wifi ที่เราสร้างขึ้น จะปรากฏชื่อ ssid และ password ใน esp terminal และต้องมีชื่อเดียวกันในรายการ wifi ที่พร้อมรับการเชื่อมต่อ

ให้เชื่อม wifi โดยเลือก ssid และใส่ password ที่ถูกต้อง ถ้าเชื่อมต่อได้สำเร็จ จะมีข้อความปรากฏ จาก source code บรรทัดใด smartphone หรือ laptop จะได้ ipaddress และอาจจะมีคำเตือนว่าไม่สามารถเชื่อมต่ออินเทอร์เน็ตได้ เนื่องจาก ESP ที่ใช้ไม่ได้ต่อกับ internet 

![image](https://github.com/user-attachments/assets/9a871ee8-1213-413e-8b94-bc473569aaea)


Build และทดสอบบนบอร์ด ESP32


![image](https://github.com/user-attachments/assets/6f5cdaad-627c-4c59-888f-1abd9c618eb1)



ผลลัพน์คือ จะเห็นว่ามีการเชื่อมต่อกับ WiFi และแสดงผลว่ามีการเชื่อมต่ออยู่ที่ไหน การเชื่อมต่อ WiFi สำเร็จ




3.ต้องการให้มีข้อความแสดงขึ้นมาหลังจากเชื่อมต่อ WiFi ได้ โดยจะขึ้นที่อยู่ของ WiFi มีขั้นตอนดังนี้


![image](https://github.com/user-attachments/assets/24a8be86-132f-492d-a719-bec0ac33a7f2)



![image](https://github.com/user-attachments/assets/c0b43f49-7f19-4087-9a7e-b967fd79976e)


ผลลัพน์คือ มีข้อความแสดงขึ้นมาจะเป็นที่อยู่ของ WiFi ที่เราเชื่อมจะแสดงเป็นชื่อและรหัสของ WiFi


สรุปผล: 



ลิงค์ Project ที่ทำบน VS code :





