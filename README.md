simple-was
===================

#### <i class="icon-file"></i> **����**

--------

 1. HTTP/1.1�� Host ��� �ؼ�
- �Ϸ�
- request ������ �Ľ��Ͽ� host ���� �ؼ��մϴ�.
- �� �ܿ��� requestUrl ���� �ؼ��Ͽ� �ٸ� ���忡 Ȱ���մϴ�.

 2. ���� ����
- �Ϸ�
- ���� ���� : **config.json**
- ���� ���� : port��ȣ, mapping ���� �����մϴ�.
- host ���� : �� host���� �ٸ� root�� html ���� ������ �����մϴ�.
- **ServerConfiguration** Ŭ�������� �� ���� ������ �а� ���� ������ ����մϴ�.

 3. 403, 404, 500 ���� ó��
- �Ϸ� 
- HTTP CODE��  key(�������Ͽ��� html���ϸ��� ã�� �� ���)�� �޾� ������ html�� ��ȯ�մϴ�.

 4. ���� ��Ģ ó��
- �Ϸ�
- ���� ��Ģ�� �߰��� ���, **AccessChecker**�� ����ü�� �����Ͽ� ó���� �� �ֽ��ϴ�.

 5. �α� ����
- �Ϸ�
- �Ϸ� ������ �α� ������ �����Ѵ�.
- �α� ������ "DEBUG"�� �����Ͽ���.
- "ERROR" ������ StackTrace�� �����.

 6. ������ WAS ����
 - �Ϸ�
 - Ŭ���� : **server.service.Hello**
 - Ŭ���������� ����
	 - parameter : "name" (default : "jisukim")
	 - http://localhost:8080/service.Hello?name=jisu
	 - http://localhost:8080/service.Hello
	 - http://127.0.0.1:8080/Hello?name=jisu
 - ���������� ����
	 - parameter : ����
	 - http://localhost:8080/super.Greeting
	 - http://127.0.0.1:8080/Greeting
- [����] localhost�� root�� server, 127.0.0.1�� server.service�� �����Ǿ� �ֽ��ϴ�. (config.json)
	  
 7. ���� �ð� ��� ����ü
- �Ϸ�
- Ŭ���� : **server.service.Time**
- http://localhost:8080/service.Time
- http://127.0.0.1:8080/Time
 8. �׽�Ʈ���̽�
 - ������ ���� ������ ����


----------
�ۼ��� : ������(kjs9298@naver.com)
