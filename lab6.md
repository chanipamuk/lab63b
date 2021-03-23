# การทดลองที่ 6 เรื่องการเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)
## วัตถุประสงค์
1. เพื่อให้นักศึกษารู้ขั้นตอนในการอัปโหลดโปรแกรมลงใน Microcontroller ESP-01
2. เพื่อให้นักศึกษารู้ว่าบอร์ด ESP-01 สามารถเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)
## อุปกรณที่ใช้
* บอร์ด ESP-01 (microcontroller)
* สาย USB
* USB to Serial port
## ศึกษาข้อมูลเบื้องต้น
* [Github ของอาจารย์ชุมพล](https://github.com/choompol-boonmee/lab63b)
* [คลิปการทดลองที่ 6](https://www.youtube.com/watch?v=T26DVHePlTs)
## วิธีการทำการทดลอง
 1. ทำการต่อสาย USB เข้ากับตัว USB to Serial port 
 2. ต่อ ESP-01 เข้ากับตัว Serial port
 3. เข้าโปรแกรม เพื่อทำการรันโปรแกรม 
 4. ใช้คำสั่ง cd เพื่อทำการ path ไปยังโฟลเดอร์ที่ทำการบันทึก codeไว้ โดยจะต้องมีการตั้งชื่อให้กับไวไฟ,กำหนด IP ฤddress local, กำหนด IP ฤddress gateway,กำหนด IP ฤddress subnet จะมีรายละเอียดดังต่อไปนี้ดังต่อไปนี้ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab6/LAB6_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_0.jpg?raw=true)
 5. เตรียม เว็บเซอร์เวอร์ 1 ตัว แล้วกำหนดค่าต่างๆตามรูปต่อไปนี้  ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab6/LAB6_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_1.jpg?raw=true)
 6. หลังจากนั้นใช้คำสั่ง `pio run -t upload` เพื่อทำการอัปโปรแกรมลงใน Microcontroller ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab6/LAB6_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_2.jpg?raw=true)
 7. ในระหว่างรอการอัปโหลดให้ทำการกดปุ่มสีดำและปุ่ม Reset บริเวณ Microcontroller เพื่อให้ Microcontroller รับโปรแกรมใหม่เข้าไป 
 8. เมื่อลงโปรแกรมเสร็จ Microcontroller สร้าง Wifi AP ขึ้นมา![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab6/LAB6_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_3.jpg?raw=true)
 9. ใช้คำสั่ง `pio run device monitor` แล้วกด reset ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab6/LAB6_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_4.jpg?raw=true)
 10. ทดสอบโดยลอกใช้โทรศัพ์ค้นหา Wifi ที่เราได้สร้างไว้
## การบันทึกผลการทดลอง
* ผลการทดลองเมื่อทำการรันโปรแกรมที่ลงเสร็จ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab6/LAB6_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_5.jpg?raw=true)
## อภิปรายผลการทดลอง
* จากผลการทดลองที่เกิดขึ้นจะเห็นได้ว่าเมื่อทำการรันโปรแกรมตามคำสั่งที่ได้เขียนและอัปโหลดลงใน Microcontroller ซึ่งผลลัพธ์ที่เกิดขึ้นคือ Microcontroller จะทำหน้าที่เป็น Wifi AP ได้
## คำถามหลังการทดลอง
* คำถาม เราสามารถเปลี่ยนชื่อ Access Point ได้หรือไม่เเล้วต้องทำอย่างไร
* ตอบ เเก้ไข code บรรทัดที่ 4 เปลี่ยนจาก "TUENG-ESP-WIFI" เป็น "ชื่อ WI-FI ที่เราต้องการให้ผู้ใช้เห็น"![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab6/LAB6_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_0.jpg?raw=true)



