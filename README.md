1.	     	1. Waterfall ตลอดระยะเวลาการพัฒนาจะไม่เห็น product ที่ส่งให้ลูกค้าเลยจะเห็น product จริงๆ ก็ถึงระยะ phase สุดท้ายแล้ว ในขณะที่ Agile ส่ง working software (ซอฟต์แวร์ที่ใช้งานได้จริง) ให้ดูว่า นี้คือสิ่งที่ลูกค้าต้องการหรือไม่ ลูกค้าจะสามารถเปลี่ยน requirement ได้ทันที ดังนั้น Agile รองรับการ เปลี่ยนแปลงของ requirement ได้ดี 
		2. Waterfallมีค่าใช้จ่ายในการรันprojectเพิ่มขึ้นเรื่อยๆเพราะrequirementเปลี่ยนแปลงอยู่ ตลอดเวลา หาก requirement ถูกเปลี่ยนในขณะที่อยู่ใน phase coding หรือ design จะมีค่าใช้จ่ายเพิ่ม ขึ้นกว่า phase แรก ๆ ยิ่งถ้า product นั้นเสร็จแล้ว มีการเปลี่ยนแปลง requirement เพิ่มเติม ค่าใช้จ่าย จะสูงมาก ในขณะที่ Agile จะ fix ค่าใช้จ่ายในการรัน project ไว้คงที่ตลอด
		3. Waterfallมีความเสี่ยงในระยะphaseสุดท้ายมากเพราะมีโอกาสที่productออกมาแล้วไม่ใช่ สิ่งที่ลูกค้าต้องการ ทำให้มีโอกาส project fail ได้สูง ในขณะที่ Agile รับความเสี่ยงตั้งแต่ต้น เพราะ การส่งมอบ product ครั้งแรกอาจไม่ใช่สิ่งที่ลูกค้าต้องการ ดังนั้นจึงปรับเปลี่ยนเรื่อยๆ จนความเสี่ยงลดลง
2.	ผมคิดว่าผมเห็นด้วยเพราะการทำงานบน Git นั้นมันมีความสะดวกในการทำงานเป็นทีมและง่ายต่อการแก้ไขในจุดต่างๆทีละจุดได้และปัจจุบันมีการทำงานบน Git อย่างแพร่หลายแล้ว
3.	$ git checkout -b Feature1 master
	$ git push -u origin Feature1
	$ git checkout master
	$ git pull origin master
4.	ถือว่ารุ่นพี่ทำบุญมาดีเพราะการ merge แล้วไม่เกิดการ conflict นั้นเป็นอะไรที่เป็นไปได้ยากมากๆ
การ merge จะทำ เมื่อเรา branch เพื่อไปทำ  feature ต่างๆ และต้องการ merge กลับมา ยัง repo กลาง
conflict จะเกิดขึ้น เมื่อโปรแกรมเมอร์ 2 คน มาทำงานไฟล์เดียวกัน และแก้ไขโค้ดให้แตกต่างกัน
วิธีการแก้ conflict  คือ 1.ให้หัวหน้าตัดสินใจ  2. พูดคุยกันในทีม
5.	abcde"a".."e" 
6.	ข้อดีของ Web Application
•	ข้อมูลจัดเก็บที่เดียว ง่ายต่อการจัดการ และไม่เกิดความซ้ำซ้อน
•	ไม่ต้องการเครื่องคอมพิวเตอร์ประสิทธิภาพสูงซึ่งมีราคาแพง
•	อยู่ที่ไหนก็ทำงานได้เพราะสามารถล๊อกอินเข้าใช้
ข้อเสียของ Web Application
•	รูป ร่างหน้าตา และการใช้งานมีได้จำกัด อาจไม่เหมาะกับงานบางประเภทที่ต้องการรูปแบบโปรแกรมที่แตกต่างจากโปรแกรม ทั่วไปเช่น โปรแกรมตกแต่งรูป โปรแกรมตัดต่อวีดีโอ
•	เว็บแอพหลายๆตัวต้องการอินเตอร์เน็ตในการใช้งานเสมอ (มีบางตัวที่สามารถทำงานออฟไลน์ได้ด้วยเช่น Gmail)
ส่วนข้อความข้างต้นผมคิดว่าน่าจะเป็นSoftware ที่ติดตั้ง install ลงที่ตัวเครื่องผ่านหน่วยความจำขนาดจำกัดอย่าง CD ซึ่งปัจจุบันมีอยู่ให้เห็นน้อยมาก ด้วยพื้นที่ที่จำกัด  และราคาที่สูง แต่ก้ยังมีข้อดีตรงที่หาซื้อง่าย ประหยัด แต่สุดท้าย web app ก้ยังมีข้อจำกัดในหลายจุดเหมือนกัน
7.	1. เริ่มจาก Client ส่ง Request ไปที่ WebApp ซึ่งจะถูกส่งต่อให้ Controller  
    ทำการตรวจสอบข้อมูลที่มาให้ (Request Method, Request Parameters) 
	2. แล้ว Controller จะเรียก Method ให้ทำงานเพื่อจัดการ Request นั้น 
	3. Model จะทำการคำนวณและอาจติดต่อกับ Database เพื่อจัดการกับ Request  
    นั้น แล้วส่งผลลัพธ์กลับไปที่ Controller 
	4. เมื่อ Controller ได้ผลลัพธ์จาก Model แล้วก็ใช้ผลลัพธ์นั้นส่งต่อให้ View ทำงาน 
	5. View จะสร้าง Page สำหรับแสดงผลลัพธ์นั้น แล้วส่ง page กลับไปที่ Controller  
	6. Controller ส่ง Page นั้น (เป็น Response) กลับไปยัง Client

8.	Rails เป็น Web Framework มีลักษณะเป็น MVC (Model-View-Controller) ถูกออกแบบมาให้มีการใช้งานที่ง่ายและรวดเร็ว ลดปัญหางานทีี่ต้องทำซ้ำๆ ทำให้ได้ productivity ที่สูงขึ้น สอดคล้องกับ Methodology แบบ Agile และมีแนวความคิดพื้นฐานคือ 
•	Don't Repeat Yourself (DRY) อะไรที่อยู่แล้ว ก็ไม่มีความจำเป็นต้องทำสิ่งนั้นซ้ำ
Reusable นั้นเอง Convention over configuration คือข้อตกลงที่ Rails
แต่ก็ไม่ได้มีข้อเสียไปเสียทีเดียว ความยุ่งยากหลายประการของ Ruby on Rails ก็มีอยู่หลายข้อคือ
	1.	การติดตั้ง Ruby on Rails บนเครื่อง development ยุ่งยากกว่าเครื่องมืออื่นๆ เช่น PHP, Java หรือ .NET
	2.	การ Deploy Rails application ขึ้นเซิร์ฟเวอร์จริง ก็ยิ่งยุ่งยากมากกว่าการติดตั้งบนเครื่อง development
	3.	ความเร็วในการทำงานของภาษา Ruby จัดได้ว่าช้ากว่าคู่แข่งอยู่มาก มีความพยายาม แก้ปัญหานี้จากหลายๆ ฝ่าย เช่น JRuby เป็นการใช้ Java Virtual Machine มารันโปรแกรมที่เขียนขึ้นด้วยภาษา Ruby อาศัยการทำงานของ Java Hotspot Compiler ในการช่วยเพิ่มความเร็วในการทำงาน
	4.	ทั้ง Ruby และ Ruby on Rails มีทัศนคติที่ไม่ดีกับ Microsoft Windows การส่งเสริมการ ทำงานบน Windows จึงมีไม่มากนัก ทำให้การพัฒนา Ruby on Rails ต้องทำบน Linux หรือ Apple Mac OS เป็นหลักและ Deploy ขึ้น Linux Server เป็นหลัก
	5.	Ruby on Rails ได้รับความนิยมมากในต่างประเทศ แต่ในประเทศไทยเพิ่งเริ่มมีความนิยมในระยะเวลา 1-2 ปีมานี้ ทำให้ตำรับตำราต่างๆ เป็นภาษาต่างประเทศทั้งหมด
	Angular JS เป็น Framework ที่ถูกพัฒนามาให้ใช้คู่กับ MVC Framework โดยเฉพาะครับ ซึ่งมันมีผลดีกับการทำ REST API ซึ่งเหมาะสำหรับคนที่เข้าใจ MVC ครับ 
ไม่คิดอะไรมากก้ server ก็ Rails จบในตัวเอง นี่แหละ ง่ายดี
9.	Heroku เป็น Platform as a Service (Paas) ที่ให้เราใช้งานได้ฟรี (มีแบบเสียเงินด้วย) โดยรองรับภาษาโปรแกรมที่หลากหลาย เช่น Ruby, PHP, Node.js, Python, Java, Clojure, Scala และยังสามารถสร้าง buildpack สำหรับภาษาอื่นๆได้ เช่น Lua ที่รันอยู่บน OpenResty ได้อีกด้วย
Heroku เหมาะกับใครบ้าง? จริงๆแล้ว มันเหมาะกับทุกคนแหละ เช่น นักศึกษาอยากลองเขียนเว็บด้วย PHP แต่ไม่ได้เช่า Hosting ก็สามารถใช้ Heroku ได้ หรือแม้แต่บริษัท Start up ที่ไม่อยากวางเครื่องเอง คอนฟิกเอง ก็ใช้ได้ เพราะมันสามารถ scale ให้รองรับผู้ใช้เยอะๆได้โดยง่าย
นอกจากรองรับภาษาโปรแกรมที่หลากหลายแล้ว ตัว Heroku มี App Store ของมันด้วยเรียกว่า add-ons สำหรับเพิ่มเติมบริการอื่นๆเข้าไปในแอปของเรา เช่น PostgreSQL, MongoDB, Redis เป็นต้น ซึ่งก็มีทั้งฟรี และไม่ฟรีให้เลือกใช้งาน
10.	 ในการพัฒนาระบบสารสนเทศในองค์กรจะต้องมีการวิเคราะห์กระบวนการทํางานของ องค์กร การพัฒนาระบบในองค์กรเป็นหน้าที่ของนักวิเคราะห์ระบบที่จะต้องทําการติดต่อ กับหน่วยงานที่ต้องการพัฒนาระบบสารสนเทศ ว่าการทํางานมีองค์ประกอบอะไรบ้าง เช่นขนาดขององค์กร รายละเอียดการทํางาน ถ้าเป็นบริษัทขนาดใหญ่นักวิเคราะห์จะต้องเข้าใจให้ชัดเจนเกี่ยวกับมาตรฐาน การทํางาน กระบวนการทํางาน ดังนั้นวิขา software development จึงมีประโยชน์ในอนาคตในการพัฒนาโปรแกรมภายในองค์กร ได้นั้นเอง


