## CA 테크놀러지스

### API Academy - Mehdi Medjaoui

##### 풀 라이프사이클 API 관리와 마이크로서비스 아키텍처를 위한 API

- 웹 사이트로 서비스를 제공하던 방식에서 벗어나 현재 여러가지 디지털 채널을 통해 서비스를 제공하는 방식으로 변화하고 있습니다. 방식이 변화함에 따라 디지털 채널과 제공되어 져야할 로직간의 원활한 커뮤니케이션을 위해 API가 고려되어져야한다고 생각합니다.

1. 비지니스와 IT 혁신을 위한 API 전략
   - Usecase 토대로 고려한 API 설계 및 개발

   - 인프라 및 Back-end 기술은 변할 수 있지만 인터페이스는 바뀌지 않게 설계

   - 마켓플레이스, 솔루션 전시, 공유등을 이용한 홍보효과 고려

   - API를 통해 모든 비지니스 플랫폼 및 장치에 데이터를 손쉽게 제공할 수 있음

   - 다양한 소스의 API를 결합하여 고유한 새 어플리케이션을 구축할 수 있음

     (새로운 비지니스 기회 창출, 타 API는 우리의 새로운 서비스가 될 수 있음)

2. 다수의 API 관리 방안 : API 프로그램을 위한 관리 및 거버넌스

   Strategy

   - Usecase 정의

   - API의 Plan 및 Strategy 설정
   - 비지니스 전략 수립 (홍보, Marketplace 고려)

   Design

   - 사용자(개발자)의 관점, 설계시 인프라에 대한 관점 반영 필요

   - Decoupling 할 수록 관리 포인트 Up
   - API Vocabulary
     - Data는 같지만 표현이 달라질 수 있음 -> 규격 표준화 필요 

   Documentation

   - 모든 API에 대해 어느 누구든 사용법을 알 수 있게 문서화 해야함

     (API에 대한 설명, URI, Parameter 정의, Error 코드, Request, Response..etc) 

   Virtualization 

   - API 배포 방식에 대한 고려 (VM, Container, Serverless..etc)

   Testing

   - 단위테스트
     - Request , Response, Error Code 에 대한 테스트
   - 통합테스트
     - 시나리오에 따른 통합 테스트 

   Monitoring & Management

   - API에 대한 인증, 로깅, 미터링, 빌링에 대한 통합적인 관리 필요
   - Metric : API Call 수, 응답시간, 오류율, 서비스당 Call 수 
   - 모니터링 

   Promotion Discovery 

   - API Deploy

   - 비지니스 창출, 홍보 활동

   Scalability

   - 새로운 서비스로의 확장성 고려

   Versioning

   - Fix 된 API 서비스에 대한 Versioning

