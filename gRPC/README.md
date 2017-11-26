### RPC란?
- Remote Procedure Call 의 약어로 별도의 원격 제어를 위한 코딩 없이 다른 주소 공간에서 함수나 프로시저를 실행할 수 있게함

#### gRPC?
- 구글에서 개발한 단일 범용 RPC 인프라인 Stubby에서 시작하여 오픈소스화 시키면서 구글의 내 외부 서비스 뿐만 아니라 모바일, IOT등 다양한 엔드포인트에서도 활용하기 위하여 gRPC를 만들어 사용함.
- 높은 성능의 오픈소스 범용 RPC 프레임워크
- 서비스와 메시지를 정의하기 위해 Protocol Buffers를 사용함(구글 코드 ProtoBuf 검색, 확장자가 *.proto)
- 구글에서 만든 Protocol Buffers는 JSON과 같은 데이터 통신 방식의 하나로 적은 양의 통신을 하기 위해 만들어짐

- gRPC를 사용하려면, server, client, .proto파일을 각각 정의해 줘야 함

- gRPC는 .proto라는 확장자를 가진 파일에서 어떤 클래스를 실행시킬지에 대한 연결 파일을 설정함
- service : Class
- rpc : Function
- returns : return

- message : C의 구조체와 유사함
*** gRPC홈페이지에 각 언어별 퀵스타터 설명이 존재함, 사용예제 있음

- gRPC를 사용하면 RPC코드를 자동으로 만들어줘 RPC를 사용하기 쉽게 함

- server에 서버 가동 코드를 넣고 실행시킴
- client에서는 run function에서 서버의 channel을 가져와 서비스를 이용할 stub을 만들어 가져올 수 있고, 이 stub은 .proto의 service에 만들어놓은 rpc와 같으며 rpc에 정의된 이름 그대로 타 언어에서도 함수를 사용할 수 있음

- gRPC에서 message에 정의된 각 필드의 숫자값들은 순서를 의미하는듯? 유니크해야함

- gRPC를 쓰면 일단 Proto Buffer가 압축률이 좋아, 매우 속도가 빠르고 HTTP2를 사용하기 때문에 서버와 클라이언트가 동시 양방향 처리가 가능하다는 장점이 있음(데이터형을 stream이용함)
- 이미지돌 byte단위로 처리 가능함

##### 참고자료
gRPC의 설명이 잘 되어 있는 블로그
- [https://medium.com/@goinhacker/microservices-with-grpc-d504133d191d](https://medium.com/@goinhacker/microservices-with-grpc-d504133d191d)
