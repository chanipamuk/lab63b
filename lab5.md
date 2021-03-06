# การทดลองที่ 5 เรื่องการเขียนโปรแกรมเชื่อมต่อไวไฟและเว็บเซอร์เวอร์
## วัตถุประสงค์
1. เพื่อให้นักศึกษารู้ขั้นตอนในการอัปโหลดโปรแกรมลงใน Microcontroller ESP-01
2. เพื่อให้นักศึกษารู้จักการสร้างเว็บเซอร์เวอร์ผ่านไวไฟ
## อุปกรณที่ใช้
* บอร์ด ESP-01 (microcontroller)
* สาย USB
* USB to Serial port
## ศึกษาข้อมูลเบื้องต้น
* [Github ของอาจารย์ชุมพล](https://github.com/choompol-boonmee/lab63b)
* [คลิปการทดลองที่ 5](https://www.youtube.com/watch?v=VX-QNQcO-b4)
## วิธีการทำการทดลอง
 1. ทำการต่อสาย USB เข้ากับตัว USB to Serial port 
 2. ต่อ ESP-01 เข้ากับตัว Serial port
 3. เข้าโปรแกรม เพื่อทำการรันโปรแกรม 
 4. ใช้คำสั่ง cd เพื่อทำการ path ไปยังโฟลเดอร์ที่ทำการบันทึก code ไว้ โดย code ที่ใช้จำเป็นจะต้องใส่ชื่อไวไฟและรหัสไวไฟลงไปด้วย จะมีรายละเอียดดังต่อไปนี้ ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab5/5_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_0.jpg?raw=true)![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab5/5_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_1.jpg?raw=true)
 6. หลังจากนั้นใช้คำสั่ง `pio run -t upload` เพื่อทำการอัปโปรแกรมลงใน Microcontroller ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab5/5_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_2.jpg?raw=true)
 7. ในระหว่างรอการอัปโหลดให้ทำการกดปุ่มสีดำและปุ่ม Reset บริเวณ Microcontroller เพื่อให้ Microcontroller รับโปรแกรมใหม่เข้าไป ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab5/5_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_3.jpg?raw=true)
 8. เมื่อลงโปรแกรมเสร็จ เราจะทำการเปิด เว็บ Browser แล้วกดปุ่ม Reset เพื่อให้เริ่มการทำงานใหม่ โดยเริ่มจาก ค้นหาไวไฟ เชื่อมต่อไวไฟ พร้อมบอก IP address
 9. ทำการคัดลอก IP Address ลงใน Browser เพื่อทำการทดสอบ
 10. ใช้คำสั่ง `pio run device monitor` แล้วกดปุ่ม reset จะได้เป็น IP Address เดิมที่เราได้ทำการทดสอบไปเมื่อขั้นตอนที่ 8.
## การบันทึกผลการทดลอง
* ผลการทดลองเมื่อทำการรันโปรแกรมที่ลงเสร็จ : hello1
* ผลการทดลองเมื่อทำการกด Reset ก่อนใช้คำสั่ง `pio run device monitor` : hello2,hello3,...
* ใช้คำสั่ง `pio run device monitor` แล้วกดปุ่ม reset : IP address 
## อภิปรายผลการทดลอง
* จากผลการทดลองที่เกิดขึ้นจะเห็นได้ว่าเมื่อทำการรันโปรแกรมจะทำการรันเป็น loop ไปเรื่อยๆตามคำสั่งที่ได้เขียนและอัปโหลดลงใน Microcontroller ซึ่งผลลัพธ์ที่เกิดขึ้นคือ Microcontroller จะทำการค้นหาไวไฟ เชื่อมต่อไวไฟ พร้อมบอก IP Address และหากเรากดที่ปุ่ม Reset ที่ Microcontroller เราจะได้ IP Address ก่อนหน้า
## คำถามหลังการทดลอง
* คำถาม ถ้าเราต้องการเปลี่ยนไวไฟที่เชื่อมต่ออยู่เป็นไวไฟอื่นต้องทำการเปลี่ยนจากตรงไหน
* ตอบ เปลี่ยนโดยการ เเก้ไข code บรรทัดที่ 5 เปลี่ยนจาก "HI_BMFWIFI_2.4G" เป็น "ชื่อไวไฟที่เราต้องการเชื่อมต่อ" เเละบรรทัดที่ 6 เปลี่ยนจาก "0819110933" เป็น "รหัสไวไฟที่เราต้องการเชื่อมต่อ" ![GitHub Logo](https://github.com/chanipamuk/lab63b/blob/main/image/Lab5/5_%E0%B9%92%E0%B9%91%E0%B9%90%E0%B9%93%E0%B9%92%E0%B9%93_0.jpg?raw=true)



