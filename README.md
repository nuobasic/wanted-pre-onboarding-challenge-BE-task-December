## 1-1) 사전과제 진행 가이드

- 아래 총 5 문제에 대한 해설을 작성한 뒤 Pull Request를 날려주세요.
- 문제 해설에 대한 정해진 양식은 없으며, 최대한 자세히 해설해주시면 좋습니다.
- 문제 유형은 해당 코스에서 다룰 주제들을 포함하고 있으니 완벽히 이해하시면 코스를 수강하는데 큰 도움이 될 것입니다.

**문의 사항은 사전 과제 Repository의 Issue로 등록해 주세요.*
  


## 1-2) 사전 과제

- (1) 동기와 비동기 프로그래밍에 대한 차이점을 설명해주세요.
    -동기는 데이터의 요청과 결과가 한 자리에서 동시에 일어나는 것을 말합니다.
     동기는 요청을 하면 시간이 얼마나 걸리던지 요청한 자리에서 결과가 주어져야 합니다.
     동기는 설계가 매우 간단하고 직관적이라는 장점이 있지만 결과가 주어질 때까지 아무것도 못하고 대기해야 하는 단점이 있습니다.
    
    -비동기는 동시에 일어나지 않는다는 의미입니다.
     비동기는 요청한 그 자링[서 결과가 주어지지 않습니다.
     비동기는 동기보다 복잡하지만 결과가 주어지는데 시간이 걸리더라고 그 시간 동안 다른 작업을 할 수 있어 자원을 효율적으로 사용할 수 있는 장점이 있습니다.
     
- (2) 블로킹과 논블로킹의 차이점을 설명해주세요.
  -블로킹와 논블로킹은 함수를 호출했을 때 제어권을 어떨게 처리하는냐에 따라 달라진다.
  -블로킹은 예를들어 A 함수가 B 함수를 호출하면 제어권을 A가 호출한 B에 넘겨줍니다. 제어건을 넘겨받은 B는 함수를 실행하고 A는 제어권을 넘겨줬기 때문에 실행을 잠시 멈춥니다.
   B함수 실행이 끝나면 자신을 호출한 A에게 제어권을 돌려줍니다.
   
   -논블로킹은 함수를 호출해도 제어권은 그대로 자신이 가지고 있는 것입니다.
   A 함수가 B 함수를 호출하면 B 함수는 실행되지만, 제어권은 A가 가지고 있습니다. 제어권을 가지고 있기 때문에 A는 자신의 코드를 계속 실행 합니다.
   
- (3) 본인이 주로 사용하는 언어에서 비동기 프로그래밍을 사용하는 방법을 설명해주세요.
  -javascript
    -Callback Function
    Callback Function은 특정 조건에서 실행되는 함수로, 특정 시간에 도달하거나 특정 이벤트가 실행됐을 때 시스템에서 호출하는 함수입니다.
    Callback Function을 활용한 비동기처리의 문제점은 코드가 복잡해 진다는 단점이 있습니다.
    
    -Promise
    Callback hell을 극복하기 위해 만들어진 것으로, Pending(대기), Fulfilled(이행), Rejected(실패)의 3가지 상태가 있습니다.
    
    -Async - Await
    Promise 를 좀더 쉬운 형태의 코드로 만들수 있데 하는 방법입니다.
    await는 피연산자의 값을 반환해줍니다.  await는 항상 async라는 이름의 함수 수정자가 있어야 합니다.
    
- (4) 메세지 큐를 쓰는 이유에 대하여 2가지 예시를 서술해주세요.
  -메세지 큐를 사용하는 이유는 대용량 데이터를 처리하기위해 사용합니다. 
  
  -예시
    -1) 효율을 위한 일괄 처리
    일괄 처리는 메시지 큐를 사용하는 좋은 이유다. 한 번에 1개씩, 100개씩 하는 대신 한 번에 100개의 레코드를 데이터베이스에 넣는 것이 훨씬 효율적입니다. 
    일괄처리는 트랜잭션 규모를 조정함으로써 성능을 최적화할 수 있도록 도와줍니다.
    
    -2)웹 애플리케이션 페이지로딩 시간 향상
    큐는 사용자의 요청이 빨리 완료될 수 있도록 백그라운드 스레드에서 복잡한 논리를 수행하는 데 웹 응용 프로그램에서 유용할 수 있다. 
    만약 누군가가 당신의 웹사이트에 주문을 한다면, 그것은 일어나야만 하는 많은 다른 일들을 수반할 수 있다. 
    전체 메시지 큐 시스템 및 배경 앱을 사용하지 않고 사용자에게 최소 성공과 반환을 수행하고 나머지 성공 사례를 백그라운드 스레드에서 시작하십시오.
    대부분의 프로그래밍 언어들은 지금 이것을 하는 방법을 가지고 있다. 예: Resque, Hangfire 등
    
- (5) 본인이 작성한 서버 코드가 있는 github repo 주소를 제출해주세요. (CRUD 기능을 모두 포함하여야 하며, 서버에 대한 설명을 README에 작성해주시면 더욱 좋습니다.) 
  -https://github.com/nuobasic/4_userSeller_service
- (6 - Optional) 해당 수업을 통해 꼭 배우고 싶은 주제 또는 지식이 있다면 자유롭게 서술해주세요.
