# 설치
- sudo yum install nginx
# 버전
- nginx -v
# 설정변경
- sudo vi /etc/nginx/nginx.conf
- root         /usr/share/nginx/html; 주석처리 후 원한는 경로 추가
- root 경로 변경 후 chmod 755 /home/ec2-user << 권한을 줘야함
- error_page /error.html 변경 index.html
- location = /error.html { } 변경 index.html


#  등록, 실행, 중지를
 - sudo systemctl enable nginx
 - sudo systemctl start nginx
 - sudo systemctl stop nginx
 - sudo systemctl status nginx



### DOCKER
# 설치
 - sudo docker pull nginx

# 실행
- sudo service nginx start
- /home/user/work/html << 루트경로 변경해서 사용한다.
- 포트는 8080 들어오면 80 보내주겠다.
- sudo docker run -d -p 8000:80 -v /home/user/work/html:/usr/share/nginx/html nginx
