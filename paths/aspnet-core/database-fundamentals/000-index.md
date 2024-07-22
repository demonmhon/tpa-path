# Database fundamentals

`Database หรือ ฐานข้อมูล` คือชุดของข้อมูลที่เป็นประโยชน์ซึ่งถูกรวบรวมและจัดเรียงไว้อย่างมีโครงสร้างเพื่อให้สามารถใช้ประโยชน์จากข้อมูลได้อย่างมีประสิทธิภาพ ฐานข้อมูลมักใช้ในองค์กรต่างๆ เพื่อเก็บข้อมูลที่เกี่ยวข้องกับกิจกรรมหรือธุรกิจขององค์กรนั้นๆ โดยข้อมูลในฐานข้อมูลสามารถเรียกใช้, ปรับปรุง, จัดการ และวิเคราะห์ได้ผ่านระบบการจัดการฐานข้อมูลหรือ Database Management System (DBMS).

`Database Management System (DBMS) หรือ ระบบการจัดการฐานข้อมูล` เป็นซอฟต์แวร์ที่ออกแบบมาเพื่อช่วยในการสร้าง, บำรุงรักษา, และใช้งานฐานข้อมูล มันช่วยให้ผู้ใช้สามารถเข้าถึงข้อมูล, ปรับปรุงข้อมูล, และจัดการข้อมูลในฐานข้อมูลได้อย่างมีประสิทธิภาพ รวมถึงการสืบค้นข้อมูลและการจัดการกับปริมาณข้อมูลที่ใหญ่โดยไม่จำเป็นต้องทราบถึงรายละเอียดในการจัดเก็บข้อมูลภายใน

DBMS ทำหน้าที่เป็นตัวกลางระหว่างผู้ใช้และฐานข้อมูล โดยจัดการกับทุกสิ่งตั้งแต่การแปลคำสั่งให้เข้ากับระบบฐานข้อมูล, การดูแลความปลอดภัยของข้อมูล, การสำรองข้อมูลและการกู้คืน, ไปจนถึงการเพิ่มประสิทธิภาพการเข้าถึงและการจัดการข้อมูล. DBMS สามารถจำแนกตามประเภทของฐานข้อมูลที่จัดการ เช่น ระบบการจัดการฐานข้อมูลสัมพันธ์ (RDBMS) สำหรับฐานข้อมูลสัมพันธ์, หรือ NoSQL DBMS สำหรับฐานข้อมูล NoSQL.

`Relational Database หรือ ฐานข้อมูลเชิงสัมพันธ์` คือประเภทของฐานข้อมูลที่จัดเก็บและให้การเข้าถึงข้อมูลที่เกี่ยวข้องกัน ข้อมูลในฐานข้อมูลเชิงสัมพันธ์ถูกจัดเก็บในรูปแบบของตาราง โดยแต่ละตารางประกอบด้วยแถว (rows) และคอลัมน์ (columns) ข้อมูลในแต่ละตารางสามารถเชื่อมโยงกันผ่านคีย์ (keys) ทำให้สามารถจัดเรียง ค้นหา และจัดการข้อมูลได้อย่างมีประสิทธิภาพ ฐานข้อมูลเชิงสัมพันธ์ถูกใช้กันอย่างแพร่หลายในแอปพลิเคชันต่างๆ เพื่อจัดเก็บข้อมูลที่มีโครงสร้างที่ชัดเจนและสัมพันธ์กัน.

`NoSQL Databases หรือ ฐานข้อมูล NoSQL` เป็นประเภทของฐานข้อมูลที่ถูกออกแบบมาเพื่อจัดการกับชุดข้อมูลขนาดใหญ่และมีโครงสร้างที่ไม่เป็นระเบียบหรือเปลี่ยนแปลงได้ง่าย ซึ่งต่างจากฐานข้อมูลเชิงสัมพันธ์ที่มีโครงสร้างที่ค่อนข้างตายตัวและเข้มงวด NoSQL databases ถูกออกแบบมาเพื่อเน้นความสามารถในการขยายระบบ (scalability) ทั้งในแนวนอน (horizontal scaling) และให้ประสิทธิภาพในการเข้าถึงข้อมูลที่รวดเร็ว รองรับการทำงานกับข้อมูลขนาดใหญ่และจำนวนการเข้าถึงที่สูง (high throughput)

NoSQL databases มีหลายประเภท รวมถึง:

1. **Document databases**: ข้อมูลถูกจัดเก็บในรูปแบบของเอกสาร (documents), ซึ่งมักจะใช้รูปแบบ JSON หรือ BSON ตัวอย่างเช่น MongoDB และ CouchDB.
2. **Key-value stores**: ข้อมูลถูกจัดเก็บในคู่ของคีย์และค่า (key-value pairs), ทำให้การเข้าถึงข้อมูลสามารถทำได้อย่างรวดเร็วมาก ตัวอย่างเช่น Redis และ DynamoDB.
3. **Column-family stores**: ข้อมูลถูกจัดเก็บในคอลัมน์แทนที่จะเป็นแถว ซึ่งเหมาะสำหรับการจัดเก็บข้อมูลที่มีการเข้าถึงแบบคอลัมน์เป็นหลัก ตัวอย่างเช่น Cassandra และ HBase.
4. **Graph databases**: ข้อมูลถูกจัดเก็บเป็นโหนด (nodes), เอจ (edges), และ คุณสมบัติ (properties) เพื่อสะท้อนความสัมพันธ์แบบกราฟ ตัวอย่างเช่น Neo4j และ Amazon Neptune.

NoSQL databases มักถูกใช้ในแอปพลิเคชันที่ต้องการความยืดหยุ่นในการจัดเก็บข้อมูล หรือเมื่อมีข้อมูลขนาดใหญ่และต้องการประมวลผลอย่างรวดเร็ว ทำให้เหมาะกับการใช้งานใน Big Data และ real-time analytics.

## ศึกษารายละเอียดเพิ่มเติมได้ที่:

### ภาษาไทย
- [บทสรุปฐานข้อมูล](https://www.saladpuk.com/beginner-1/database-design)
- [สอนพื้นฐาน SQL ทั้งหมดแบบจบในคลิปเดียว !! 🔥](https://www.youtube.com/watch?v=vd1qdnCX5RU)
- [ปูพื้นฐาน SQL สำหรับจัดการฐานข้อมูล 6 ชั่วโมงเต็ม [FULL COURSE]](https://www.youtube.com/watch?v=sgQiJ-8Ra8c)
- [สอน Microsoft SQL Server](https://www.youtube.com/watch?v=kh3MfhTiyQk&list=PLoTScYm9O0GH8gYuxpp-jqu5Blc7KbQVn&index=1)


### English

- [Oracle: What is a Database?](https://www.oracle.com/database/what-is-database/)
- [Prisma.io: What are Databases?](https://www.prisma.io/dataguide/intro/what-are-databases)
- [Intro To Relational Databases](https://www.udacity.com/course/intro-to-relational-databases--ud197)
- [What is Relational Database](https://youtu.be/OqjJjpjDRLc)
- [NoSQL Explained](https://www.mongodb.com/nosql-explained)
- [How do NoSQL Databases work](https://www.youtube.com/watch?v=0buKQHokLK8)