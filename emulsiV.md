# โปรแกรมแสดงตัวย่อของ ชื่อ-สกุล
- ชื่อของผมคือ Phuriphat Saejiw ดังนั้นโปรแกรมต้องรันออกมาคือ PS ซึ่งเลข ascii ที่ต้องนำไปใส่คือ 50(P) และ 53(S) ซึ่งนำสองเลขนี้ไปใส่ใน addressที่20 และหลังจากสองตัวนี้ให้ใส่ที่เหลือเป็น 00 ให้หมด

# ฟังก์ชันและการทำงาน

## ฟังก์ชัน

- addi(add imidiate) คือคำสั่งที่ใช้สำหรับบวก โดยในโปรแกรมนี้คือเอาเลข 32 + x0 โดย x0 จะเป็น 0 เสมอ แล้วนำค่าที่บวกได้ไปใส่ใน x1 และมีอีกอันนึงคือการเอา 1 + x1 และนำไปใส่ใน x1 ซึ่งหมายความว่า x1 จะเพิ่มขึ้นเรื่อยๆ

- lui(load upper imidiate) คือนำค่าซ้ายสุด 1 word หรือ 0xc0000000 มาใส่ใน x2 แค่ 20 ไบท์แรก

- beq(branch on equal) คือคำสั่งที่เช็คว่าเท่ากันมั้ย ในกรณีของโปรแกรมนี้จะเช็คว่า x3 กับ x0 เท่ากันไหม ถ้าเท่าจะบวกไป 16

- sb(store bite) คือคำสั่งเก็บหน่วยความจำ ในกรณีของโปรแกรมนี้จะนำ x3 ไปเก็บที่ 0(x2)ซึ่งคือจอซ้ายล่าง

- jal(jump in link) คือคำสั่งที่จะกระโดดไป -16 ซึ่งหมายความว่าจะกระโดดถอยไปที่ address 8 และเมื่อคำสังรันตัวอักษรครบเราจะใช้คำสั่งนี้จะกระโดดกลับไปที่ 0 และจะวนไปเรื่อยๆ

## การทำงาน

- คำสั่งแรกจะนำเลข 0 มาจาก pc วางที่ bus แล้วดึงเลข 4 bite มาจาก address 0 วางไว้ที่ data จากนั้นส่งมาแปลที่ instruction แล้วนำไปใส่คำสั่ง alu ด้วย 0 ได้ 20+0 = 20 แล้วนำไปเก็บที่ x1

- คำสั่งที่ 2 เรียก 4 bite จาก address 4 มาใส่ใน data แล้วนำไปใส่ใน instruction(lui) นำเลขที่ได้ไปใส่ใน alu จากนั้นนำไปเก็บที่ x2

- คำสั่งที่ 3 เรียก 4 bite จาก address 8 มาใส่ใน data แล้วนำไปใส่ใน instruction(lbu) นำ 0+20 แล้วไปนำเลขจาก address 20 มา 1 bite ในกรณีนี้จะเป็น 50 นำเลขไปเก็บที่ x3

- คำสั่งที่ 4 เรียก 4 bite จาก address c มาใส่ใน data แล้วนำไปใส่ใน instruction(beq) เช็คว่า x3 เท่ากับ x0 มั้ยซึ่งนำไปเช็คที่ comparator

- คำสั่งที่ 5 เรียก 4 bite จาก address 10 มาใส่ใน data แล้วนำไปใส่ใน instruction(sb) นำค่า x3 ไปใส่ใน 0(x2) คือ address ของจอแสดงผลซึ่งจะโชว์ตัวอักษรของค่า x3 ออกมา

- ทำวนซ้ำจนกว่าตัวอักษรจะครบ และเมื่อครบมันจะทำการวนอยู่ที่ 1c ตลอด
