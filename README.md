프로젝트 소개
====
URL을 입력받아 짧게 줄여주고 단축된 URL 을 입력하면 원래URL 로 리다이렉트하는 서비스
* URL 입력폼 제공 및 결과 출력
* 단축URL 키는 8자 이내로 생성
* 동일한 URL 에 대한 요청은 동일한 단축URL로 응답
* 단축URL 요청받으면 원래 URL 로 리다이렉트

개발환경
----
* JAVA 1.8  
* SpringBoot 2.1.7  
* MariaDB 5.7.21  
* Gradle 5.4.1  
* JQuery 3.1.1  
* Swagger 2.0

프로세스
----
* 이미 등록된 단축URL을 생성시
![process_1](https://user-images.githubusercontent.com/33255462/63277479-61283a80-c2e0-11e9-984a-8d361eda9d97.png)

* 새로운 단축URL 생성시
![process_2](https://user-images.githubusercontent.com/33255462/63277191-de06e480-c2df-11e9-8d4a-66df71f85a2f.png)

문제해결방법
----

빌드&실행 방법
----
DDL문은 DDL.sql 이름으로 프로젝트 안에 들어가 있습니다.



현재 문제점 & 추후 개선방안
----
1. 단축URL 생성시 DB에 이미 저장된 단축 URL이 있는지 조회하고 있는대 , 악의적인 사용자가 같은URL에 대해서 연속적으로 누른다면?  
-연속적인 호출에 대해서 웹서버의 방화벽에서 막는 방법도 있다.  
-Ehcash를 적용한다. 같은 URL에 대해서는 같은 단축URL을 반환해주기 때문에 고려해볼만 하다.   

