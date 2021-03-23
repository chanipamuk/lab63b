# การทดลองที่ 2 เรื่องการเขียนโปรแกรมค้นหาไวไฟ
## วัตถุประสงค์
1. เพื่อให้นักศึกษารู้ขั้นตอนในการอัปโหลดโปรแกรมลงใน Microcontroller ESP-01
2. เพื่อให้นักศึกษารู้ว่าบอร์ด ESP-01 สามารถเขียนโปรแกรมที่ใช้สำหรับการค้นหาไวไฟได้
## อุปกรณที่ใช้
* บอร์ด ESP-01 (microcontroller)
* สาย USB
* USB to Serial port
## ศึกษาข้อมูลเบื้องต้น
* [Github ของอาจารย์ชุมพล](https://github.com/choompol-boonmee/lab63b)
* [คลิปการทดลองที่ 2](https://www.youtube.com/watch?v=yBjab0UNuB8)
## วิธีการทำการทดลอง
 1. ทำการต่อสาย USB เข้ากับตัว USB to Serial port 
 2. ต่อ ESP-01 เข้ากับตัว Serial port
 3. เข้าโปรแกรม เพื่อทำการรันโปรแกรม 
 4. ใช้คำสั่ง cd เพื่อทำการ path ไปยังโฟลเดอร์ที่ทำการบันทึก codeไว้ โดย code จะมีรายละเอียดดังต่อไปนี้ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab2/LAB2_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_0.jpg?raw=true)![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab2/LAB2_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_1.jpg?raw=true)
 5. หลังจากนั้นใช้คำสั่ง `pio run -t upload` เพื่อทำการอัปโปรแกรมลงใน Microcontroller ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab2/LAB2_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_2.jpg?raw=true)
 6. ในระหว่างรอการอัปโหลดให้ทำการกดปุ่มสีดำและปุ่ม Reset บริเวณ Microcontroller เพื่อให้ Microcontroller รับโปรแกรมใหม่เข้าไป ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab2/LAB2_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_3.jpg?raw=true)
 7. เมื่อลงโปรแกรมเสร็จ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab2/LAB2_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_4.jpg?raw=true)
 8. ใช้คำสั่ง `pio run device monitor` เพื่อดูผลลัพธ์ ซึ่งเป็นการรัน code จากข้อ 4.![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab2/LAB2_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_5.jpg?raw=true)
 9. เมื่อกดปุ่ม Reset ผลลัพธ์ที่ได้จะกลับไปเริ่มใหม่![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab2/LAB2_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_6.jpg?raw=true)
## การบันทึกผลการทดลอง
* ผลการทดลองเมื่อทำการรันโปรแกรมที่ลงเสร็จ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab2/LAB2_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_5.jpg?raw=true)
* ผลการทดลองเมื่อทำการกด Reset ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab2/LAB2_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_6.jpg?raw=true)
## อภิปรายผลการทดลอง
* จากผลการทดลองที่เกิดขึ้นจะเห็นได้ว่าเมื่อทำการรันโปรแกรมจะทำการรันเป็น loop ไปเรื่อยๆตามคำสั่งที่ได้เขียนและอัปโหลดลงใน Microcontroller ซึ่งผลลัพธ์ที่เกิดขึ้นคือ Microcontroller จะทำการค้นหาไวไฟบริเวณรอบๆ แล้วแสดงชื่อของไวไฟที่สามารถค้นหาได้ และหากเรากดที่ปุ่ม Reset ตัว Microcontroller จะเริ่มต้นการค้นหาใหม่อีกครั้ง
## คำถามหลังการทดลอง
* คำถาม หาก Microcontroller ESP-01 ค้นหาไวไฟบริเวณรอบๆไม่พบจะสามารถแสดงข้อความว่าอะไร
* ตอบ NO NETWORK FOUND



