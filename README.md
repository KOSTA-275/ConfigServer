![configServer](https://github.com/user-attachments/assets/d8ff3c2e-e1e6-42da-af4a-c483e4224936)
모든 마이크로서비스의 application.properties는 ConfigServer의 설정을 받아 설정된다.

※사용 이유는 마이크로서비스의 각자의 설정을 받지않고 중앙집중형 관리를 통해 설정을 한곳에서 관리하여 추적용이 하기 위함이다.

Config Server는 데이터를 전달하는 매개체 역할만 수행하며 실제 설정 정보를 담을 영속성의 경우 DB, 파일, Git Service를 사용한다.

여러 영속성 도구 중 Git Service를 가장 많이 사용하여 Git Repository에 properties 설정을 저장하여 관리한다.

