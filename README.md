simple-was
===================

#### <i class="icon-file"></i> **스펙**

--------

 1. HTTP/1.1의 Host 헤더 해석
- 완료
- request 정보를 파싱하여 host 정보 해석합니다.
- 그 외에도 requestUrl 등을 해석하여 다른 스펙에 활용합니다.

 2. 설정 파일
- 완료
- 설정 파일 : **config.json**
- 공통 정보 : port번호, mapping 정보 저장합니다.
- host 정보 : 각 host마다 다른 root와 html 파일 정보를 저장합니다.
- **ServerConfiguration** 클래스에서 위 설정 파일을 읽고 서비스 로직에 사용합니다.

 3. 403, 404, 500 에러 처리
- 완료 
- HTTP CODE와  key(설정파일에서 html파일명을 찾을 때 사용)를 받아 적절한 html를 반환합니다.

 4. 보안 규칙 처리
- 완료
- 추후 규칙을 추가할 경우, **AccessChecker**의 구현체를 생성하여 처리할 수 있습니다.

 5. 로깅 설정
- 완료
- 하루 단위로 로그 파일을 저장한다.
- 로그 레벨은 "DEBUG"로 설정하였다.
- "ERROR" 레벨은 StackTrace를 남긴다.

 6. 간단한 WAS 구현
 - 완료
 - 클래스 : **server.service.Hello**
 - 클래스명으로 매핑
	 - parameter : "name" (default : "jisukim")
	 - http://localhost:8080/service.Hello?name=jisu
	 - http://localhost:8080/service.Hello
	 - http://127.0.0.1:8080/Hello?name=jisu
 - 설정값으로 매핑
	 - parameter : 없음
	 - http://localhost:8080/super.Greeting
	 - http://127.0.0.1:8080/Greeting
- [참고] localhost는 root가 server, 127.0.0.1은 server.service로 설정되어 있습니다. (config.json)
	  
 7. 현재 시간 출력 구현체
- 완료
- 클래스 : **server.service.Time**
- http://localhost:8080/service.Time
- http://127.0.0.1:8080/Time
 8. 테스트케이스
 - 간단한 서비스 로직만 구현


----------
작성자 : 김지수(kjs9298@naver.com)
