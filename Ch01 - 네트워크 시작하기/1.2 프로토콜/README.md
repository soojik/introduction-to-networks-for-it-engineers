## 2. 프로토콜

네트워크에서 통신할 때의 규약을 **프로토콜**이라고 한다. 최근에는 산재되어 있던 여러 가지 프로토콜 기술이 **이더넷-TCP/IP 기반 프로토콜**들로 변경되고 있다.

- 물리적 측면: 데이터 전송 매체, 신호 규약, 회선 규격 등. 이더넷이 널리 쓰임
- 논리적 측면: 장치들끼리 통신하기 위한 프로토콜 규격. TCP/IP가 널리 쓰임

한정된 자원 때문에 최대한 적은 데이터를 이용해 프로토콜을 정의하고 사용해야 했다. 따라서  대부분의 프로토콜이 문자 기반이 아닌 2진수 비트 기반으로 만들어졌다. 비트의 위치까지 까다롭게 정하고 그 약속을 철저히 지켜야 통신을 수행할 수 있었다.

물론 애플리케이션 레벨의 프로토콜은 비트 기반이 아닌 문자 기반 프로토콜들이 많이 사용된다. HTTP와 SMTP가 대표적인 예로, HTTP 프로토콜의 헤더는 문자로 표현되어 사람이 읽을 수 있다.

```plain
GET /api HTTP/1.1
Accept: text/html, application/xhtml+xml, */*
Referer: http://zigispace.net/
Accept-Language: ko-KR
User-Agent: Mozilla/5.0 (Windows NT 6.1; WOW64; Trident/7.0; TCO_20181006113830; rv:11.0) like Gecko
Accept-Encoding: gzip, deflate
Host: theplmingspace.tistory.com
DNT: 1
Connection: Keep-Alive
```

실제 텍스트 파일과 같은 데이터가 전달되기 때문에 효율성은 비트 기반 프로토콜보다 떨어지지만 다양한 확장이 가능하다.

TCP와 IP는 별도 계층에서 동작하는 프로토콜이지만 함께 사용하고 있는데 이런 프로토콜 묶음을 **프로토콜 스택**이라고 부른다. 실제로 TCP/IP 프로토콜 스택에는 TCP와 IP 뿐만 아니라 UDP, ICMP, ARP, HTTP, SMTP, FTP 등 다양한 애플리케이션 레이어 프로토콜들이 있다.

TCP/IP 프로토콜 스택은 물리 부분인 이더넷 외에 네트워크 계층, 전송 계층, 애플리케이션 계층으로 구성된다.

<img src="TCP IP 프로토콜 스택.png" />