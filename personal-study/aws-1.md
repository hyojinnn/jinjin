# AWS

ubuntu버전은18.04

JDK, TomCat8.5.73 설치

스프링프로젝트를 war파일로 export

&#x20;&#x20;

AWS EC2 생성하기

&#x20;1\. 인스턴스 시작

&#x20;2\. AMI 프리티어 ubuntu  선택하기

&#x20;3\. 스토리지 30GB까지 무료

&#x20;4\. 보안그룹 포트범위 설정 - HTTP 80포트

&#x20;5\. 인스턴스 시작하기

&#x20;6\. 키 페어 생성



EC2 접속하기(Putty 이용하기)

1. puttygen 으로 pem -> ppk로 변경하여 private 저장
2. putty 에서 Host Name ubuntu@IP주소
3. ssh -> auth 에서 private키 road       &#x20;

AWS 인스턴스에 자바 설치하기

1. sudo apt-get install openjdk-8-jdk -> open jdk 설치
2. javac -version -> 설치확인
3. which javac readlink -f /usr/bin/javac -> javac 위치확인
4. sudo vi /etc/profile -> 관리자권한으로 profile 열기
5. export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64 -> profile 내용 맨 하단에 JAVA\_HOME 설정_
6. source /etc/profile -> 환경설정 소스 적용
7. echo $JAVA\_HOME -> 적용            &#x20;

ubuntu에 톰캣 설치하기

1. &#x20; 톰캣사이트에서 tar.gz 파일 우클릭 후 링크를 복사하기

[https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.73/bin/apache-tomcat-8.5.73.tar.gz](https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.73/bin/apache-tomcat-8.5.73.tar.gz)



2\. wget [https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.73/bin/apache-tomcat-8.5.73.tar.gz](https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.73/bin/apache-tomcat-8.5.73.tar.gz)

명령어를 통해 압축파일을 다운로드&#x20;



3\. tar -xvzf apache-tomcat-8.5.73.tar.gz

압축파일 압축해제



4\. 톰캣 구동하기

cd apache-tomcat-8.5.73/

./bin/startup.sh



5\. 톰캣이 실행되었는지 확인하기

netstat -tnlp             &#x20;
