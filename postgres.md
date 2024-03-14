# postgres 다운로드
sudo docker pull postgres

# 도커 볼륨생성
sudo docker volume create postgres

# postgres 실행
sudo docker run -p 5432:5432 --name postgres -e POSTGRES_PASSWORD=qwer1234! -d -v postgres:/var/lib/postgresql/data postgres
리턴 데이터
dad68d9a80b835a77d8cf668db3052c6bdce2c649dc0ec3752b8a5fedc3bd475

# postgres 접속
sudo docker exec -it postgres /bin/bash
- psql -U postgres 명령어
- psql (13.0 (Debian 13.0-1.pgdg100+1)) 리턴
- Type "help" for help. 리턴
- postgres=# SELECT * FROM PG_USER; 명령어

# 사용자 생성
  - CREATE USER seongwon PASSWORD '1q2w3e4r' SUPERUSER;
