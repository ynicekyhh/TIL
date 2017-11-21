### RPC란?
- Remote Procedure Call 의 약어로 별도의 원격 제어를 위한 코딩 없이 다른 주소 공간에서 함수나 프로시저를 실행할 수 있게함

### gRPC?
- 구글에서 개발한 단일 범용 RPC 인프라인 Stubby에서 시작하여 오픈소스화 시키면서 구글의 내 외부 서비스 뿐만 아니라 모바일, IOT등 다양한 엔드포인트에서도 활용하기 위하여 gRPC를 만들어 사용함.
- 높은 성능의 오픈소스 범용 RPC 프레임워크
- 서비스와 메시지를 정의하기 위해 Protocol Buffers를 사용함(구글 코드 ProtoBuf 검색, 확장자가 *.proto)
- 구글에서 만든 Protocol Buffers는 JSON과 같은 데이터 통신 방식의 하나로 적은 양의 통신을 하기 위해 만들어짐

##### 참고자료
gRPC의 설명이 잘 되어 있는 블로그
- [https://medium.com/@goinhacker/microservices-with-grpc-d504133d191d](https://medium.com/@goinhacker/microservices-with-grpc-d504133d191d)
