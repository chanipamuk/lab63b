# การทดลองที่ 1 เรื่องการเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์
## วัตถุประสงค์
1. เพื่อให้นักศึกษารู้ขั้นตอนในการอัปโหลดโปรแกรมลงใน Microcontroller ESP-01
2. เพื่อให้นักศึกษารู้ว่าบอร์ด ESP-01 สามารถเขียนโปรแกรมที่ใช้สำหรับการนับเลขได้
## อุปกรณที่ใช้
* บอร์ด ESP-01 (microcontroller)
* สาย USB
* USB to serial port
## ศึกษาข้อมูลเบื้องต้น
* [Github ของอาจารย์ชุมพล](https://github.com/choompol-boonmee/lab63b)
* [คลิปการทดลองที่ 1](https://www.youtube.com/watch?v=NLIUsWLEpmg)
## วิธีการทำการทดลอง
 1. ทำการต่อสาย USB เข้ากับตัว USB to serial port 
 2. ต่อ ESP-01 เข้ากับตัว Serial port
 3. เข้าโปรแกรม เพื่อทำการรันโปรแกรม 
 4. ใช้คำสั่ง cd เพื่อทำการ path ไปยังโฟลเดอร์ทำการบันทึก codeไว้ โดย code จะมีรายละเอียดดังต่อไปนี้ดังต่อไปนี้ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab1/LAB1_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_0.jpg?raw=true)
 5. หลังจากนั้นใช้คำสั่ง `pio run -t upload` เพื่อทำการอัปโปรแกรมลงใน microcontroller ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab1/LAB1_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_1.jpg?raw=true) 
 6. ในระหว่างรอการอัปโหลดให้ทำการกดปุ่มสีดำและปุ่ม Reset บริเวณ microcontroller เพื่อให้ microcontroller รับโปรแกรมใหม่เข้าไป ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab1/LAB1_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_2.jpg?raw=true)
 7. เมื่อลงโปรแกรมเสร็จ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab1/LAB1_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_3.jpg?raw=true)
 8. ใช้คำสั่ง `pio run device monitor` เพื่อดูผลลัพธ์ ซึ่งเป็นการรัน code จากข้อ 4.![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab1/LAB1_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_4.jpg?raw=true)
 9. เมื่อกดปุ่ม reset ผลลัธ์ที่ได้จะกลับไปเริ่มใหม่![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab1/LAB1_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_5.jpg?raw=true)
## การบันทึกผลการทดลอง
* ผลการทดลองเมื่อทำการรันโปรแกรมที่ลงเสร็จ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab1/LAB1_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_4.jpg?raw=true)
* ผลการทดลองเมื่อทำการกด Reset ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab1/LAB1_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_5.jpg?raw=true)
## อภิปรายผลการทดลอง
* จากผลการทดลองที่เกิดขึ้นจะเห็นได้ว่าเมื่อทำการรันโปรแกรมจะทำการรันเป็น loop ไปเรื่อยๆตามคำสั่งที่ได้เขียนและอัปโหลดลงใน microcontroller ซึ่งผลลัพธ์ที่เกิดขึ้นคือการนับโดยเพิ่มจำนวนทีละ 1 ไปเรื่อยๆ ไม่สิ้นสุด จนกว่าเราจะกด Reset เพื่อทำการเริ่มต้นนับ 1 ใหม่
## คำถามหลังการทดลอง
* คำถาม หากต้องต้องการให้เพิ่มจำนวนนับทีละ 10 ต้องทำอย่างไร
* ตอบ แก้ไข code บรรทัดที่ 12 จาก cnt++; เป็น cnt+10; ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab1/LAB1_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_0.jpg?raw=true) 



