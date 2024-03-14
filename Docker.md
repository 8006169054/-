# - AWS EC2
-- root 권한이 아닐경우 sudo 사용한다.
sudo dnf update
- 설치
sudo dnf install docker -y

# Docker 서비스 시작
sudo systemctl start docker

# Docker 서비스 작동 상태 확인
sudo systemctl status docker

# Docker 서비스를 운영체제 부팅시 자동 시작하도록 설정
sudo systemctl enable docker

# docker 명령어를 sudo 없이 사용하기 위해 계정을 docker 그룹에 소속 (계정 재접속 필요)
sudo usermod -aG docker $USER
newgrp docker

docker --version

# docker network 대역 변경하기 (연결이 안될 시 체크 사항)
https://waspro.tistory.com/635

cat /etc/docker/daemon.json
{
"log-driver": "journald",
"log-opts": {
"tag": "{{.Name}}"
},
"bip": "172.26.0.1/16" << IP 대역 변경
}
