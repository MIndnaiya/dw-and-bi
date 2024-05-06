04-Building a Data Lake


ขั้นตอนการทำงาน
เปิด terminal run
docker-compose up
เปิด port 8888 จะเข้าไปที่หน้า jupyterlab

copy token ใน terminal ไปใส่ใน Key

จะเข้าสู่หน้า jupyterlab มี folder work ที่ประกอบด้วยไฟล์

actors
data
events
img
output_csv
output_parquet
repos
workshop
docker-compose.yml
etl_local_with_s3.ipynb
etl_local.ipynb
etl.ipynb
README.md
โดยข้อมูลจาก folder data file github_events_01.json และ github_events_02.json จะถูกดึงไปอยู่ในรูปแบบตารางที่ folder

   actors ได้ file ประกอบด้วยข้อมูล
    actor.login
    id as event_id
    actor.url as actor_url
   events ได้ folder: date=2022-08-17 และ file ประกอบด้วยข้อมูล
    id
    type
    created_at
    day(created_at) as day
    month(created_at) as month
    year(created_at) as year
    date(created_at) as date
   repos ได้ file ประกอบด้วยข้อมูล
    repo.name
    id as event_id
    repo.url as repo_url
   output_csv และ output_parquet folder: year=2022 ได้ file ประกอบด้วยข้อมูล
    id
    type
    created_at
    to_date(created_at) as date
    year(created_at) as year
    actor.login
    actor.url as actor_url
    repo.name
    repo.url as repo_url
