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