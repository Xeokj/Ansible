master ip = 192.168.56.107   
worker ip = 192.168.56.114   

# 231031  
1. 플레이북 internet.yml 파일을 생성하고 실행
2. 관리 호스트에서 진행해야 할 사항  
   - firewalld, httpd, mariadb, php, php-mysqlnd 패키지를 없으면 설치하는 작업
   - firewalld를 실행하는 작업
   - 80번 포트를 현재와 영구적으로 추가하는 작업
   - mariadb를 실행하는 작업

# 231101  
## 과제 1
1. 아래의 내용  '변수 = 값' 형태로 yaml 파일에 지정하기  
   - web_pkg: httpd  
   - fireall_pkg: firewalld  
   - web_service: httpd  
   - firewall_service: firewalld  
   - python_pkg: python3-PyMySQL  
   - rule: httpd  
2. web_pkg, firewall_pkg, python_pkg를 설치하기
3. firewall_service를 실행하고 재부팅하고 실행하기
4. web_service를 실행하고 재부팅하고 실행하기
5. 방화벽에 rule 서비스를 허용하는 플레이를 작성하고 관리 호스트의 웹 서버로 정상 접근이 가능한지 확인하기
  
## 과제 2
1. secret.yml 파일을 만들고 redhat 암호화를 이용하여 시크릿 파일 생성하기
2. ansible-vault edit은 비밀번호가 걸려있는 시크릿 파일을 수정할 때 사용하는 명령어이며 해당 명령어를 이용하여 secret.yml 파일을 수정하기
   — secret.yml 파일은 아래와 같이 하기  
   username: ansibleuser1  
   pwhash: $6$teieRsZEt$qidtmsktjiamdskjastiasmkdmQ
3. secret.yml 파일의 변수를 이용하여 ansibleuser1 유저를 생성하고 pwhash를 사용하여 비밀번호를 지정하는 create_user.yml 파일 제작  


# 231102  
## 과제 1  
변수 packages 하위에 dhcp, bind를 등록하고, 각 패키지에 맞는 서비스를 추가 등록하여 반복문을 사용하여 패키지를 실행하는 플레이북 생성 및 실행하기  

## 과제 2  
abc 변수에 저장된 1이 0보다 작거나 ansible_distribution이 RedHat이 아니라면 실패했다는 메시지를 출력(fail 모듈 사용)  

## 과제 3  
웹 서비스와 ftpd를 재시작하는 핸들러를 만들고 mariadb가 실행 중이라면(조건) 웹 서비스와 ftpd를 순차적으로(반복) 재시작  


   
