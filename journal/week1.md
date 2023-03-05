# Week 1 — App Containerization

### Containerize Application
Test Python without Docker

```sh 
cd backend-flask
export FRONTEND_URL="*"
export BACKEND_URL="*"
python3 -m flask run --host=0.0.0.0 --port=4567
cd ..
```
- Unlocked Port 4567
- Opened link in browser, working
- Added 'api/activities/home'
- Received json output

Create Dockerfile

![image](https://user-images.githubusercontent.com/26598534/222984485-4c0bcd4e-809c-481b-954c-74b050296cd8.png)

Create and Run Container using docker-compose.yml script

![image](https://user-images.githubusercontent.com/26598534/222984688-c66617bc-93ba-4053-a61f-211c7982a08c.png)

Get Container IDs and Images

![image](https://user-images.githubusercontent.com/26598534/222984759-505ce1bc-d28c-48ec-a4cb-427107daf12f.png)

Test server

![image](https://user-images.githubusercontent.com/26598534/222984890-e51c0c24-ed33-45f2-bd72-e91060873494.png)

### Update open API to add notifications

https://github.com/schalkwbs/aws-bootcamp-cruddur-2023/commit/6bc6ee485f56c4ae7bf9b62e580972d6be06b7e0

### Create new notifications backend endpoint

https://github.com/schalkwbs/aws-bootcamp-cruddur-2023/commit/097981546602326f45d74262a144bc36d0434e8c

### Implement frontend notifications page (for some reason this committed twice, adding both)

https://github.com/schalkwbs/aws-bootcamp-cruddur-2023/commit/5f7362456f3a4442216a49af99eb36ec5f9d113c
https://github.com/schalkwbs/aws-bootcamp-cruddur-2023/commit/c8d959bb64b55ba19c6424ad0a4cacfddba1b433

### Added minor Notifications page fixes 

https://github.com/schalkwbs/aws-bootcamp-cruddur-2023/commit/afe211da141d2e61bd319533baa3899be07e0438

### Run DynamoDB local container and ensure it works

![image](https://user-images.githubusercontent.com/26598534/222986682-94bd6956-2c6e-4ce5-98c5-1315601af1d8.png)
![image](https://user-images.githubusercontent.com/26598534/222986689-c5ead484-034c-48b5-849b-d7390a105934.png)

### Run Postgres Container and ensure it works

Install Postgres client on Gitpod

```sh
  - name: postgres
    init: |
      curl -fsSL https://www.postgresql.org/media/keys/ACCC4CF8.asc|sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/postgresql.gpg
      echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" |sudo tee  /etc/apt/sources.list.d/pgdg.list
      sudo apt update
      sudo apt install -y postgresql-client-13 libpq-dev
 ```
Ensure Postgres container works

```sh
gitpod /workspace/aws-bootcamp-cruddur-2023 (main) $ psql -h localhost -U postgres
Password for user postgres: 
psql (13.10 (Ubuntu 13.10-1.pgdg20.04+1))
Type "help" for help.

postgres=# \l
                                 List of databases
   Name    |  Owner   | Encoding |  Collate   |   Ctype    |   Access privileges   
-----------+----------+----------+------------+------------+-----------------------
 postgres  | postgres | UTF8     | en_US.utf8 | en_US.utf8 | 
 template0 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
 template1 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
(3 rows)

postgres=# 
```
![image](https://user-images.githubusercontent.com/26598534/222987190-47a6e2b5-e58b-4938-9123-ac2013056ce0.png)
![image](https://user-images.githubusercontent.com/26598534/222987745-5c726dcf-8b4a-4b44-a477-4163d0ffaafe.png)

