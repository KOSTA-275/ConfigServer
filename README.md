# 깃 접근 설정
Git Repository로 어플리케이션 프로퍼티 설정 공유하기 위해 Git Repository 하나 생성
깃 배쉬에 ssh-keygen -m PEM -t rsa -b 4096 -C “코멘트” 를 작성하여 비대칭키를 생성 비대칭키는 사용자/.ssh 경로에 생성
![image](https://github.com/user-attachments/assets/e6a314a3-ffd2-45a4-8e68-213f692bfb14)
Add deploy key에 비대칭키를 추가
![image (1)](https://github.com/user-attachments/assets/ad481332-97db-4cc0-8d7f-eeed0345943c)
Repository에 키 생성완료.

# 중앙관리 설정
모든 마이크로서비스의 application.properties는 ConfigServer의 설정을 받아 설정된다.

# 필수 의존성
빌드 도구 : build.gradle

Config Server 의존성
<br>
dependencies {
	implementation 'org.springframework.cloud:spring-cloud-config-server'
 }
 <br>
마이크로 서버 의존성 
<br>
dependencies {
	implementation 'org.springframework.cloud:spring-cloud-starter-config'
 }

# 사용 이유
마이크로 서비스의 각자의 설정을 받지않고 중앙집중형 관리를 통해 설정을 한곳에서 관리하여 추적용이 하기 위함이다.

# ConfigServer는 데이터를 전달하는 매개체
실제 설정 정보를 담을 Git Service를 가장 많이 사용하여 Git Repository에 properties 설정을 저장하여 관리하였다.

# 시스템 아키텍처
![화면 캡처 2024-11-03 174141](https://github.com/user-attachments/assets/afbfbbfa-e134-48f7-a93b-9efd6fc529a6)
