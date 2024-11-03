![화면 캡처 2024-11-03 174141](https://github.com/user-attachments/assets/afbfbbfa-e134-48f7-a93b-9efd6fc529a6)
# 중앙관리 설정
모든 마이크로서비스의 application.properties는 ConfigServer의 설정을 받아 설정된다.

# 사용 이유
마이크로서비스의 각자의 설정을 받지않고 중앙집중형 관리를 통해 설정을 한곳에서 관리하여 추적용이 하기 위함이다.

# ConfigServer는 데이터를 전달하는 매개체
실제 설정 정보를 담을 Git Service를 가장 많이 사용하여 Git Repository에 properties 설정을 저장하여 관리하였다.

