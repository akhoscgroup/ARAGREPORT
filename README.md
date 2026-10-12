# ARAGREPORT — Customer AR Aging Analyzer

เครื่องมือวิเคราะห์อายุลูกหนี้ (AR Aging) จากไฟล์ Excel ที่ Export จาก SAP
(Manage Customer Line Items → Layout FIN_AR) ทำงานบนเบราว์เซอร์ทั้งหมด ไม่ต้องติดตั้งโปรแกรม และไม่มีการส่งข้อมูลออกไปภายนอก

## วิธีใช้
1. เปิดไฟล์ `index.html` ด้วยเบราว์เซอร์
2. Step 1: เลือกไฟล์ Excel และติ๊กกลุ่มลูกหนี้ (ALL / ในเครือ / พนักงาน / การค้า)
3. Step 2: เลือก Base Date และ Key Date
4. Step 3: กำหนดช่วงวัน Overdue 7 ช่วง
5. กด "คำนวณ Aging Report" แล้วกด "ดาวน์โหลดไฟล์ Excel"

## ความสามารถ
- คำนวณ Due Date จาก Base Date + Payment Terms และแบ่งอายุหนี้ 7 ช่วง
- คอลัมน์ **Invoice**: Journal Entry Type = UC ใช้ Reference Key 3, อื่นๆ ใช้ Original Reference Document
- จัดกลุ่มลูกหนี้จากรหัสลูกค้า: ขึ้นต้น 3 = ในเครือ, ขึ้นต้น 14 = พนักงาน, อื่นๆ = การค้า
- Export Excel 3 แท็บ: AR_AG, PIVOT, Original
