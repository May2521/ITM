ปัญหา 1
/////////////
ข้อที่ 2 

HTML url = http://localhost/dashboard/howto.html
method = GET
Status code = 200 OK

CSS url = http://localhost/dashboard/stylesheets/normalize.css
method = GET
Status code = 200 OK (from memory cache)

js url = http://localhost/dashboard/javascripts/modernizr.js
method = GET
Status code = 200 OK (from memory cache)

รูปภาพ url = http://localhost/dashboard/images/social-icons.png
method = GET
Status code = 200 OK (from memory cache) 

////////////

ข้อ 3
url = http://localhost/dashboard44/phpinfo.php
method = GET
Status code = 404 Not Found

//////////

ข้อที่ 4
 ควรใช้  GET หรือ POST 
 เพราะอะไร
 ตวรใช้ POST  เพราะ การยืนยันคำสั่งซื้อเป็นการสร้างข้อมูลแถวใหม่ในตารางหักสต็อกและตัดเงินในซึ่งตามมาตรฐาน HTTP คำสั่ง GET มีไว้สำหรับอ่านข้อมูลโดยห้ามแก้ไขข้อมูลฝั่งเซิร์ฟเวอร์ ส่วนการสร้างรายการใหม่หรือประมวลผลธุรกรรมต้องใช้ POST

//////////////

 ข้อ 5
 จาก Presentation Layer, Business Logic Layer,Data Layer การทำงานของเว็บแอปเหล่านี้ อยู่ในชั้นใด
 หารแสดงรูปสินค้า / Presentation
 การคำนวนค่าจัดส่งสินค้า / Business Logic
 การเก็บประวัติการสั่งซื้อ / Data 
 การตรวจสต๊อก / Business Logic

 /////////////

 ปัญหา 2
 2.1 อธิบายทำไมลูกค้าจึงแก้ราคาสืนค้าได้
 เมื่อระบบไม่ได้ทำการ ตรวจสอบและคำนวณราคาซ้ำในฝั่ง Server (Server-Side Validation) ก่อนบันทึกลงฐานข้อมูล ผู้ใช้งานจึงสามารถใช้เครื่องมือ Developer Tools (เช่น Inspect Element หรือ F12) เพื่อแก้ไขค่าตัวเลขราคาใน HTML ก่อนกดส่งข้อมูล (Submit) ทำให้ระบบบันทึกราคาที่ถูกแก้ไขโดยไม่ได้รับอนุญาตได้

 2.2 งานต่อไปนี้ควรอยู่ในฝั่งใด
 ตรวจสอบ Email / Client-Side(และ Server-Side)
 คำนวนยอดชำระ / Server-Side
 ตรวจสต๊อก / Server-Side
 แสดงเมนูแบบเลื่อน / Client-Side
 ตรวจสอบสิทธ์ของพนักงาน / Server-Side
 เตือนเมื่อลืมป้อนค่าลงในช่อง / Client-Side

 2.3 เสนอทางป้องกันการแก้ไขราคาสินค้าโดยลูกค้า
 ย้ายการดึงราคามาไว้ที่ Server-Side: เมื่อลูกค้ากดสั่งซื้อ ให้ส่งเฉพาะ รหัสสินค้า (Product ID) และ จำนวน (Quantity) ไปยังเซิร์ฟเวอร์ จากนั้นให้เซิร์ฟเวอร์เป็นผู้ค้นหาราคาสินค้าจริงจากฐานข้อมูลด้วยตนเอง ห้ามรับค่า "ราคา" ตรงมาจากฝั่ง Client
ทำ Server-Side Validation: ตรวจสอบความถูกต้องของข้อมูลทั้งหมดที่ส่งมาจากผู้ใช้ฝั่งเซิร์ฟเวอร์ทุกครั้งก่อนนำไปประมวลผลหรือบันทึก
เข้ารหัสหรือใช้งาน Token: หากจำเป็นต้องส่งข้อมูลสำคัญผ่านฟอร์ม ควรมีการเข้ารหัส (Encryption) หรือใช้ Token (เช่น CSRF Token / Session) เพื่อตรวจสอบความสมบูรณ์ของข้อมูล

 2.4 php ควรทำงานที่ด้านใดของระบบ
ฝั่งที่ควรทำงาน: Server-Side (ฝั่งเซิร์ฟเวอร์)
คำอธิบาย: PHP เป็นภาษาที่ถูกออกแบบมาเพื่อประมวลผลบนเซิร์ฟเวอร์ (Server-Side Scripting Language) ทำหน้าที่ติดต่อฐานข้อมูล ประมวลผลตรรกะทางธุรกิจ (Business Logic) และสร้างหน้า HTML ส่งกลับไปแสดงผลที่บราวเซอร์ของผู้ใช้งาน
//////////
ปัญหาที่ 3 
3.3
PHP Version 8.2.12
3.4
PDO Driver for MySQL	enabled
Client API version	mysqlnd 8.2.12

3.5
mbstring
Multibyte Support	enabled