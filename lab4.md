# การทดลองที่ 4 เรื่อง การเขียนโปรแกรมอินพุทสัญญาณดิจิทัล
## วัตถุประสงค์
1. เพื่อให้นักศึกษารู้ขั้นตอนในการอัปโหลดโปรแกรมลงใน Microcontroller ESP-01
2. เพื่อให้นักศึกษารู้ว่าเราสามารถนำอินพุทจากภายนอกเข้ามาใน Microcontroller ESP-01 ได้
## อุปกรณที่ใช้
* บอร์ด ESP-01 (microcontroller)
* สาย USB
* USB to Serial port
* Adapter
* สาย port 0 และ port 1
* LED เปล่งแสง
* เซนเซอร์แสง + ตัวต้านทาน
## ศึกษาข้อมูลเบื้องต้น
* [Github ของอาจารย์ชุมพล](https://github.com/choompol-boonmee/lab63b)
* [คลิปการทดลองที่ 4](https://www.youtube.com/watch?v=nFqoZT26U5k)
## วิธีการทำการทดลอง
 1. ทำการต่อสาย USB เข้ากับตัว USB to Serial port 
 2. ต่อ Adapter เข้ากับตัว Serial port โดย Adapter นั้นจะต่อเข้ากับ port 0 และ port 1 ซึ่งต่อเข้ากับ LED เปล่งแสง
 3. ต่อ Microcontroller ESP-01 เข้ากับ Serial port 
 4. เข้าโปรแกรม เพื่อทำการรันโปรแกรม 
 5. ใช้คำสั่ง cd เพื่อทำการ path ไปยังโฟลเดอร์ที่ทำการบันทึก codeไว้ โดย code จะมีรายละเอียดดังต่อไปนี้ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_0.jpg?raw=true)
 6. หลังจากนั้นใช้คำสั่ง `pio run -t upload` เพื่อทำการอัปโปรแกรมลงใน Microcontroller ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_1.jpg?raw=true)
 7. ในระหว่างรอการอัปโหลดให้ทำการกดปุ่มสีดำและปุ่ม Reset บริเวณ Microcontroller เพื่อให้ Microcontroller รับโปรแกรมใหม่เข้าไป ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_2.jpg?raw=true)
 8. เมื่อลงโปรแกรมเสร็จ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_3.jpg?raw=true)
 9. ใช้คำสั่ง `pio run device monitor` เพื่อดูผลลัพธ์ ซึ่งเป็นการรัน code จากข้อ 5 ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_4.jpg?raw=true)
 10. จากนั้นนำสายไฟ port 0 ต่อเข้ากับเส้นสีดำ (0 โวลล์)![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_5.jpg?raw=true)
 11. เมื่อกดปุ่มสีดำบริเวณ USB to Serial port ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_6.jpg?raw=true)
 
 เมื่อใช้ Microcontroller ESP-01 (ที่ทำการลงโปรแกรมแล้ว) ต่อเข้ากับ เซนเซอร์แสง + ตัวต้านทาน แล้ว port 0 ที่ต่อเข้ากับเส้นสีดำ (0 โวลล์)![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_7.jpg?raw=true)![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_8.jpg?raw=true)
## การบันทึกผลการทดลอง
* ผลการทดลองเมื่อทำการรันโปรแกรมที่ลงเสร็จ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_4.jpg?raw=true)
* ผลการทดลองเมื่อนำสายไฟ port 0 ต่อเข้ากับเส้นสีดำ(0 โวลล์) ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_5.jpg?raw=true)
* ผลการทดลองเมื่อทำการต่อ Microcontroller ESP-01 (ที่ทำการลงโปรแกรมแล้ว) ต่อเข้ากับ เซนเซอร์แสง + ตัวต้านทาน ที่ต่อเข้ากับเส้นสีดำ (0 โวลล์)![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_7.jpg?raw=true)![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab4/LAB4_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_8.jpg?raw=true)
## อภิปรายผลการทดลอง
* จากผลการทดลองที่เกิดขึ้นจะเห็นได้ว่าเมื่อทำการรันโปรแกรมจะทำการรันเป็น loop ไปเรื่อยๆตามคำสั่งที่ได้เขียนและอัปโหลดลงใน Microcontroller ซึ่งผลลัพธ์ที่เกิดขึ้นคือ LED เปลงแสงจะเปิดและปิดไฟขึ้นอยู่กับสายไฟ port 0  และหากต่อ Microcontroller ESP-01 (ที่ทำการลงโปรแกรมแล้ว) ต่อเข้ากับ เซนเซอร์แสง + ตัวต้านทาน แล้ว port 0 ที่ต่อเข้ากับเส้นสีดำ (0 โวลล์) ไฟที่เปิดปิดจะขึ้นอยู่กับสภาพแวดล้อมว่าเป็นเช่นไร ( เปิด/เมื่อมีแสง และ ปิด/เมื่อไม่มีแสง)
## คำถามหลังการทดลอง
* คำถาม ถ้าต้องการให้เมื่อมีเเสงสว่างมากจะให้ LED เปล่งเเสงดับ มีเเสงสว่างน้อยให้ LED เปล่งเเสงติดต้องทำอย่างไร
* ตอบ เปลี่ยน code บรรทัดที่ 19 จาก digitalWrite(2, LOW) เป็น digitalWrite(2, HIGH) เเล้วก็๋บรรทัดที่21 จาก digitalWrite(2, HIGH) เป็น digitalWrite(2, LOW)

