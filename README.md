# Tik Tac Toe (XO) Project 

จากโจทย์ 
1. ให้เขียนเกม XO ด้วย Web หรือ Mobile App โดยให้เกมสามารถกำหนด ขนาดตารางของ XO นอกจาก 3x3 เป็นขนาดใด ๆ ก็ได้

2. มีระบบฐานข้อมูลเก็บ history play ของเกมเพื่อดู replay ได้

3. ส่งโค้ดกลับมาผ่าน github public link พร้อม readme วิธีการ setup, run โปรแกรม, วิธีออกแบบโปรแกรมและ algorithm ที่ใช้

4.  โจทย์ bonus point มี AI ระบบ bot คู่ต่อสู้ ที่เล่นกับมนุษย์อัตโนมัติได้ [โจทย์นี้เป็น optional ทำหรือไม่ทำก็ได้]


## การ Setup
* ตรวจสอบการติดตั้งของ flutter ภายในเครื่อง
* ตรวจสอบการทำงานของอุปกรณ์ หรือ Emulator

## การ Run
* Run บนอุปกรณ์ Android หรือ Android Emulator 

## การออกแบบโปรแกรม
* แยกโครงสร้างเป็น 3 ส่วน ได้แก่
    * ส่วน Algorithm - เป็นส่วนโครงสร้างสำหรับการทำงานของ Minimax
    * ส่วน Main - ใช้สำหรับเรียก ฟังก์ชัน และ สร้างส่วนของ GUI
    * ส่วน Local database - สำหรับเก็บข้อมูลประวัติผล โดยใช้ sql lite
      
* สร้างผู้เล่น 2 ส่วน
    * ส่วนของผู้เล่น (X)
    * ส่วนของ Algorithm(BOT) (O)

## Algorithm 
### Minimax Algorithm
เลือกใช้ Minimax Algorithm เพราะ เป็น Algorithm ที่สามารถใช้ในการตัดสินใจในการเล่น Tic Tac Toe(XO) ได้ดี เนื่องจาก Algorithm ต้องการที่จะให้ฝั่งของตนมีความได้เปรียบกว่าอีกฝั่งเลยต้องมีการคำนวณค่าที่ดีที่สุดให้ตนเองเพื่อได้เส้นทางที่ดีที่สุดในการเล่น Tic Tac Toe(XO) 

### หลักการทำงาน
 * Minimax ทำงานด้วยการทำซ้ำ หรือ Loop เรียกฟังก์ชันตัวเอง เพื่อสร้าง search tree 
 * Maximzing และ Minimizing Player ผู้เล่นที่พยายามให้คะแนนสูงสุดและผู้เล่นที่พยายามให้คะแนนต่ำสุด
 * การคำนวณ แต่ละรอบของการเรียกฟังก์ชัน Minimax จะคำนวณคะแนน แต่ละเหตุการณ์ที่เป็นไปได้ และเลือกค่าที่ดีที่สุดหรือค่าที่แย่ที่สุดของแต่ละผู้เล่น
 * เลือกเส้นทางที่ดีที่สุด แต่ละรอบของการเรียกใช้ฟังก์ชัน Minimax ผู้เล่น Maximzing จะเลือกค่าที่มากที่สุดจากการคำนวณทุกเส้นทาง และ ผู้เล่น Minimizing จะเลือกค่าที่น้อยที่สุด


## ปัญหาที่พบ
* พบข้อผิดพลาดของการทำงานในส่วนของการขยายตาราง
* เรื่องการเก็บ database ส่วนของ replay





 
