03-Building a Data Warehouse-2
folder นี้ประกอบด้วย 1 folder 4 file
etl.py
github_events_01.json
README.md
requirements.txt
folder ENV

ขั้นตอนการทำงาน
Google Cloud
สร้าง Project
Create dataset เป็นเหมือนกล่องไว้เก็บ table ในที่นี้ตั้งชื่อว่า github (เป็นข้อมูลเกี่ยวกับ github)
Create service account ที่ IAM & Admin เพื่อสร้าง Key และกำหนด role ในที่นี้กำหนดเป็น Bigquery admin
เมื่อสร้างเสร็จ file จะถูก download แล้วนำมาใส่ใน folder credentials ที่ github
github
เปิด terminal run
python -m venv ENV
source ENV/bin/activate
pip install -r requirements.txt

เพื่อ install และ activate requirements.txt
ปรับ file etl.py ตรง keyfile และ project_id ให้ตรงกับใน Project Google Bigquery
    keyfile = "../credentials/deft-seat-413911-swu-ds525-load-data-to-bigquery-e8564c2fefe5.json"
    
    project_id = "deft-seat-413911"
run file etl.py
python etl.py 
จะได้ file github_events.csv ใน folder 03-building-a-data-warehouse-2 ใน Github
จะได้ table events ใน dataset github ใน Google Bigquery
