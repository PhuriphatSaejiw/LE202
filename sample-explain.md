# Sample Explain

## Experiment 1

![153397439-e3f3030f-ecf4-4d7b-a5e5-20418d6a5710](https://user-images.githubusercontent.com/98943440/154242954-68360494-795e-468b-ad11-5c830f911161.png)

มีสองส่วน ส่วนsetup จะรันครั้งเดียว set serial port ที่ความเร็ว115200 

อีกส่วนคือส่วน loop ที่ให้เพิ่มตัวแปลcount ขึ้นเรื่อยๆ 

และให้หน่วงเวลา 1 นาที

## Experiment 2

![image](https://user-images.githubusercontent.com/98943440/154243647-21a49d03-95fe-4c20-8184-2e405cbf2567.png)

ส่วน set up เริ่มต้นให้count เป็น 0 และทำการเซ็ต wifi ให้พร้อมใช้งาน โดยมี delay 100 ms

ส่วน loop จะแสดงข้อความเริ่มแสกนหาสัญญาณ wifi ถ้าไม่เจอจะขึ้น no network found ถ้าเจอจะขึ้นให้เลือกใช้สัญญาณ

## Experiment 3

![image](https://user-images.githubusercontent.com/98943440/154244588-9ddb7fe4-9218-4baf-99bd-6302c5c35763.png)

ส่วน set up เริ่มต้นให้count เป็น 0 และกำหนดให้ port 0 เป็น output

ส่วน loop ให้นับจำนวน count ไปเรื่อยๆ และเมื่อ count เป็นเลขคู่จะแสดงข้อความว่า on และจะทำให้ไฟติด แต่ถ้าเป็นเลขคู่ จะแสดงว่า off และไฟจะดับ

โดยมีdelay 500 ms


## Experiment 4

![image](https://user-images.githubusercontent.com/98943440/154245333-bc5e8119-fb73-4a48-afc2-be04bf9da5c1.png)

เซ็ต port 0 เป็น input และ 2 เป็น output 

ส่วน loop จะทำการอ่านค่าport 0 ถ้าอ่านได้ 1 จะส่ง low ไปที่ port 2 ซึ่งจะทำให้ไฟดับ แต่ถ้าอ่านได้ 1 จะส่ง high ไปยัง port2 จะทำให้ไฟติด

## Experiment 5

![image](https://user-images.githubusercontent.com/98943440/154245971-f0bfe5c5-7a1e-4470-9ef1-b7c7693dab72.png)

โปรแกรมต้องเชื่อมต่อกับ wifi ดังนั้นต้องใส่ SSID และ Password เข้าไป จากนั้นเลือก server แล้วจะเริ่มรับสัญญาณ โดยมี delay 500 ms

หลังจากนั้นจะแสดง ip address ถ้าไม่ได้จะแสดง path not found ถ้าได้จะแสดง Hello cnt:

## Experiment 6

![image](https://user-images.githubusercontent.com/98943440/154246617-06d31358-24cd-459c-8983-3e0dc2ae8952.png)

![image](https://user-images.githubusercontent.com/98943440/154246628-2dcd39d2-99ec-419c-8b16-fb3bca9e1605.png)


กำหนด ชื่อ password ipaddress gateway และ subnet

เปิดเซิร์ฟเวอร์ที่พอร์ต 80 

ถ้าได้จะแสดง Hello cnt: แต่ถ้าไม่ได้ จะแสดง path not found 

เมื่อเซิร์พเวอร์เริ่มจะแสดง HTTP server started




