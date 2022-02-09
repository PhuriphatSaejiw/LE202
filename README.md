# LE202
## 01Digital

- สัญญาณดิจิทัลรับสัญญาณ 0v เป็น 0 และ สัญญาณระหว่าง 0v ถึง 5v เป็น 1

                       
- ข้อมูลดิจิทัลจะรับข้อมูลด้วยเลขฐาน 2 หรือ 16

## 02Voltage

-แรงดันไฟฟ้า มีแบบกระแสตรง เช่น แบตเตอรี่ ไฟที่ออกจากคอมพิวเตอร์ etc. และแบบกระแสสลับ เช่น ไฟบ้าน

## 03Computer

-มีการพัฒนาคอมพิวเตอร์มาอย่างยาวนาน ตั้งแต่ 50-60 ปีที่แล้ว จากที่มีรูปร่างใหญ่จนทำให้เล็กลงมาจนถึงทุกวันนี้ และยังมีความเร็วและความจุที่มากขึ้น

## 04Internet 

-ทำให้ทุกอย่างสามารถเชื่อมต่อกันได้ทั่วโลก ทั้งแบบไร้สายและมีสาย เช่น wifi bluetooth 4G 5G

## 05Program Lang

-ภาษาคอมพิวเตอร์ เช่นภาษาซี จาวา ไพธอน

## Platform IO

-โปรแกรมคอมพิวเตอร์ขนาดเล็ก (ไมโครคอนโทรเลอร์)

-IO เป็นมาตรฐานการพัฒนาซอฟแวร์แบบใหม่ ที่สามารถเขียนโปรแกรมในระบบไมโครคอนโทรเลอร์ได้หลายแบบ

-มีบอร์ดในท้องตลาดกว่า 900 แบบที่สารถนำไปพัฒนาต่อได้

## 07IO set

-เริ่มจากดาวน์โหลดโปรแกรม git

-เปิด command prompt เลือกโฟลเดอร์ แลัวรันคำสั่ง gitclone https://github.com/chompool-boonmee/ioset1.git

-แล้วหลังจากนั้นทำตามที่ github เขียนไว้

# Experiment

## Experiment 1

-ไมโครคอนโทรเลอร์ ESP01 มีcpu มีเสาอากาศรับwifi มีอุปกรณ์ต่อusb เพื่อไปยัง serial

-ในโปรแกรมทดสอล มีสองส่วน ส่วนsetup จะรันครั้งเดียว set serial port ที่ความเร็ว115200 อีกส่วนคือส่วน loop ที่ให้เพิ่มตัวแปลcount ขึ้นเรื่อยๆ และให้หน่วงเวลา 1 นาที

-ในการอัปโหลดโปรมแกรมเข้าไปยัง esp01 ต้องกดปุ่มพอร์ต0 และกดรีเซ็ต

-โปรแกรมแสดงผลลัพธ์ ตัวแปร count จะแสดงผลลัพธ์จาก 0 เพิ่มขึ้นทีละ 1 สามารถกดรีเซ็ตได้

## Experiment 2

-หลังจากเสียบ serial port แล้ว ก็เตียม set up wifi

-และโปรแกรมจะแสกนหา wifi 

## Experiment 3 relay

-เมื่อติดตั้งโปรแกรมจะทำให้ส่งสัญญาณผ่านพอร์ต 0 ไปยังหลอดไฟ ทำให้หลอดไฟกระพริบ

-เมื่อนำคอนโทรเลอรืมาเสียบกับ relay มันจะส่งสัญญาณ 0 1 เข้าไปใน relay เพื่อ เปิด ปิด สวิตซ์ เมื่อมันทำงานเราจะได้ยินเสียงโลหะเปิดปิด

## Expriment 4 

-เป็นการทดลองนำ input จากภายนอกมายังไมโครคอนโทรเลอร์

-สัญญาณ input ที่พอร์ต 0 จะเป็นตัวควบคุม (อ่าน 0 ไฟติด อ่าน 1 ไฟดับ)

-ทดลองต่อเซนเซอร์แสง มีresistorในวงจร โดยต่อขาฝั่งหนึงเข้ากับสายดิน

-เมื่อเซนเซอร์เจอแสง จะอ่านเป็น 0 ไฟจะติดและถ้าเอานิ้วปิดจะอ่านเป็น 1 ไฟจะดับ

## Experiment 5 wifi

-โปรแกรมต้องเชื่อมต่อกับ wifi ดังนั้นต้องใส่ SSID และ Password เข้าไป

-เมื่ออัปโหลดโปรแกรมเข้าไมโครคอนโทรเลอร์ เช็คการทำงานของโปรแกรมด้วยเว็บบราวเซอร์

-จะทำงานก็ต่อเมื่อเจอเว็บบราวเซอร์ และจะแสดงข้อความ Hello cnt :

## Experiment 6 wifi ap

-ตัวคอนโทรเลอร์เป็นตัวปล่อย wifi

-ต้องกำหนด ชื่อ password ipaddress gateway และ subnet

-เปิดเซิร์ฟเวอร์ที่พอร์ต 80 และเตีรียมเว็บเซิร์ฟเวอร์ไว้ 1 ตัว

