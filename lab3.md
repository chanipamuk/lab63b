# การทดลองที่ 3 เรื่องการเขียนโปรแกรมเอ้าพุทสัญญาณดิจิทัล
## วัตถุประสงค์
1. เพื่อให้นักศึกษารู้ขั้นตอนในการอัปโหลดโปรแกรมลงใน Microcontroller ESP-01
2. เพื่อให้นักศึกษารู้ว่าบอร์ด ESP-01 สามารถเขียนโปรแกรมที่สามารถแสดงผลลัพธ์ในรูปแบบของสัญญาณดิจิตอลได้
3. เพื่อให้นักศึกษารู้ว่า relay สามารถทำหน้าที่เป็นสวิทต์ เปิด-ปิด LED เปล่งแสง
## อุปกรณที่ใช้
* บอร์ด ESP-01 (microcontroller)
* สาย USB
* USB to Serial port
* Adapter
* สาย port 0 และ port 1
* LED เปล่งแสง
* relay
## ศึกษาข้อมูลเบื้องต้น
* [Github ของอาจารย์ชุมพล](https://github.com/choompol-boonmee/lab63b)
* [คลิปการทดลองที่ 3.1](https://www.youtube.com/watch?v=CCnN1WJsXQY)
* [คลิปการทดลองที่ 3.2](https://www.youtube.com/watch?v=6JnhaUILGuw) 
## วิธีการทำการทดลอง
 1. ทำการต่อสาย USB เข้ากับตัว USB to Serial port 
 2. ต่อ Adapter เข้ากับตัว Serial port โดย Adapter นั้นจะต่อเข้ากับ port 0 และ port 1 ซึ่งต่อเข้ากับ LED เปล่งแสง
 3. ต่อ Microcontroller ESP-01 เข้ากับ Serial port ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_0.jpg?raw=true)![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_1.jpg?raw=true)
 4. เข้าโปรแกรม เพื่อทำการรันโปรแกรม 
 5. ใช้คำสั่ง cd เพื่อทำการ path ไปยังโฟลเดอร์ที่ทำการบันทึก codeไว้ โดย code จะมีรายละเอียดดังต่อไปนี้ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_2.jpg?raw=true)
 6. หลังจากนั้นใช้คำสั่ง `pio run -t upload` เพื่อทำการอัปโปรแกรมลงใน Microcontroller ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_3.jpg?raw=true)
 7. ในระหว่างรอการอัปโหลดให้ทำการกดปุ่มสีดำและปุ่ม Reset บริเวณ Microcontroller เพื่อให้ Microcontroller รับโปรแกรมใหม่เข้าไป ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_4.jpg?raw=true)
 8. เมื่อลงโปรแกรมเสร็จ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_5.jpg?raw=true)
 9. ใช้คำสั่ง `pio run device monitor` เพื่อดูผลลัพธ์ ซึ่งเป็นการรัน code จากข้อ 5 ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_6.jpg?raw=true)
 10. เมื่อกดปุ่ม Reset ผลลัพธ์ที่ได้จะกลับไปเริ่มใหม่![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_7.jpg?raw=true)
 
 เมื่อใช้ Microcontroller ESP-01 (ที่ทำการลงโปรแกรมแล้ว) ต่อเข้ากับ relay โดย relay จะทำหน้าที่เป็นสวิตท์ให้กับวงจร(เปิด-ปิดLED เปล่งแสง) ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_8.jpg?raw=true)
## การบันทึกผลการทดลอง
* ผลการทดลองเมื่อทำการรันโปรแกรมที่ลงเสร็จ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_6.jpg?raw=true)
* ผลการทดลองเมื่อทำการกด Reset ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab3/LAB3_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_7.jpg?raw=true)
## อภิปรายผลการทดลอง
* จากผลการทดลองที่เกิดขึ้นจะเห็นได้ว่าเมื่อทำการรันโปรแกรมจะทำการรันเป็น loop ไปเรื่อยๆตามคำสั่งที่ได้เขียนและอัปโหลดลงใน Microcontroller ซึ่งผลลัพธ์ที่เกิดขึ้นคือ LED เปลงแสงจะสลับเปิดและปิดไฟไปเรื่อยๆไม่สิ้นสุด และหากเรากดที่ปุ่ม Reset ที่ Microcontroller จะเริ่มต้นการรันใหม่อีกครั้ง
## คำถามหลังการทดลอง
* คำถาม ตัว Microcontroller ESP-01 สามารถเปลี่ยนเวลาำงานทุก 0.5 วินาทีเป็น 7 วินาทีได้ไหม ทำอย่างไร
* ตอบ โดยการเเก้ไข code บรรทัดที่ 23 จาก delay(500) เป็น delay(7000)


