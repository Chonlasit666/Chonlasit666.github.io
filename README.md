# CN331AS2 สมาชิกกลุ่มประกอบไปด้วย 
 - นาย ชลสิทธิ์ มูลคร 6110613020
 - นาย ปฐมพงศ์ วนาสันติพงศ์ 6210612856
 
### โฟลเดอร์ CN331AS2 ประกอบไปด้วย 2 ส่วนหลักๆคือ 
 - cn331 : เป็นโฟลเดอร์หลักของโปรเจค ประกอบไปด้วย Settings ที่เก็บค่า Static เเละ Urls ซึ่งไว้ link กับส่วนต่างๆของโปรเจคนี้  
 - register : เป็นโฟลเดอร์ที่เก็บ application หลักซึ่งประกอบไปด้วย model database เเละ views ในการคำนวน เเละส่งออกการเเสดงผลไปยัง HTML  

### อื่นๆได้เเก่  
 - media : เป็นส่วนที่ไว้เก็บไฟล์จำพวก Image เพื่อใช้เเสดงผลในหน้า Profile ของผู้ใช้  
 - static : เป็นส่วนที่ไว้เก็บไฟล์จำพวก CSS เเละ Image เพื่อใช้ในการเเสดงผลบน HTML  

### องประกอบของ Model
#### Subject มีหน้าที่เก็บข้อมูลได้แก่
- รหัสวิชา (subject_id)  
- ชื่อวิชา (subject_name)  
- เทอม (semester)  
- ชั้นปี (year)  
- จำนวนที่นั้งทั้งหมด (max_seat)  
- วิชาเปิดเรียนอยู่หรือไม่ (available)  
                             
#### Student มีหน้าที่เก็บข้อมูลได้แก่   
- ผู้ใช้งาน (user) ส่วนนี้จะไปดึงขอมูลจาก User model ของ django  
- วิชา (Subject) ส่วนนี้จะไปเชื่อมโยงกับ DataBase ของ subject เป็นลักษณะ Many to Many  
- ชื่อไฟล์รูป (title)   
- รูป (img)  


### องประกอบของ views  
 - info : เป็นส่วนที่ไว้แสดงผลในหน้าโปรไฟล์ของผู้ใช้งาน  
 - index : เป็นส่วนที่ใช้เเสดงผลรายวิชาก่อนจะเข้าสู่หน้าดูรายระเอียดวิชา  
 - login_view : หน้าเข้าใช้งานระบบ  
 - logout_view : หน้าออกจากระบบ  
 - subject_info : จัดการเกี่ยวกับรายละเอียดวิชา  
 - enroll : ฟังค์ชั่นที่ไว้รับผู้ใช้งานเข้าสู่ฐานข้อมูล  
 - unenroll : ฟังค์ชั่นที่ไว้ลบผู้ใช้งานออกจากฐานข้อมูล    
 - upload : ฟังค์ชั่นที่ไว้อัพโหลดรูปภาพของผู้ใช้งาน    
 - admin_subject_info : ฟังค์ชั่นที่ไว้ใช้สำหรับ Superuser ในการดูนักศึกษาในระบบ
 
 | Username | password | Role |
 | -------- | -------- | ---- |
 | 6210612851 | maneemenaa | User |
 | 6210612852 | maneemenaa | User |
 | 6210612853 | maneemenaa | User |
 | 6210612854 | maneemenaa | User |
 | 6210612855 | maneemenaa | User |
 | 6210612856 | maneemenaa | User |
 | 6210612857 | maneemenaa | User |
 | 6210612858 | maneemenaa | User |
 | 6210612859 | maneemenaa | User |
 | admin | admin | Superuser |
 
 ----------------------------------------------------------------------------------
 
 | Subject_ID | Subject_name | Status |
 | ---------- | ------------ | ------ |
 | cn201 | Object Oriented Programming | Not Available |
 | cn202 | Data Structure I | Available |
 | cn203 | Data Structure II | Available |
 | cn204 | Probability and Static | Not Available |
 | cn240 | Data Science | Not Available |
 | cn101 | Basic Programming | Available |
 | cn200 | Discreate Math | Not Available |
 
