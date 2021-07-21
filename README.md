# kubernetes-study

도커란?  
Container 기반의 오픈소스 가상화 플랫폼. 
실행환경을 Container로 추상화. 
OS가상화 (VM은 HW가상화). 
Host와 Kernel 을 공유함 (VM보다 얕게 격리된다). 
Docker-engine위에 App과 필요한 binary만 올라가고, 커널은 공유하므로 VM보다 Volumn이 작다. 
(VM은 하이퍼바이저 위에, Guest OS, binary, App 3가지 + 커널 공유X). 
Image Volumn이 작다는 것은 Network를 덜 사용한다는 것 -> Cloud 사용량 감소. 
내 개발환경에서 운영image를 만들어 배포하면 끝이다. 
컨테이너 오케스트레션 --> microservices 발전의 토대 마련. 
  
쿠버네티스란?  
다수의 컨테이너를 관리하기 위한 컨테이너 오케스트레이션
무중단 서비스(Pod)
무중단 배포(Rolling Update, 새로운 버전의 Pod를 생성한 후 이전 Pod 삭제)
Scale Out (트래픽양에 따라 Pod의 개수를 조정한다)
