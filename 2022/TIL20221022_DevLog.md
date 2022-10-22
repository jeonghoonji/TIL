# 20221022 개발일지

# 오늘 공부한 내용 😀

- 데이터베이스 이상 현상, 정규화, 관계 대수 용어 정리
- kakao API 데이터 응답 값 문자열로 추출 작업
- 지도에 출발지, 목적지 마커 표시
- kakaoSDKNavi 기능 구현 시도!
- Swift components / split 사용법 차이점
- 프로그래머스 0단계

# 어려웠던 내용🤯

- kakaoSDKNavi 사용법
- 문자열 처리하는 두 문제에서 관련 메서드 사용법

# 궁금한 내용 / 부족한 내용🤔

- Swift에서 사용하는 문자열 관련해서 처리하는 메서드 공부를 하고 정리해 보기
- kakaoSDKNavi 좌표계 이야기가 나와 알아봐야 할 거 같음

# 느낀점🤨

데이터베이스를 공부를 다시 시작하면서 정규화 부분을 이해하고 넘어갈 수 있었다.

이번 정리로 관계 대수 개념도 알게 되었다.

API 데이터 응답 값을 전처리하는 과정이 한 달가량 해결하지 못해 개발 진도가 나아가질 않았는데 오늘 해결하여 통쾌했다!

kakaoSDKNavi 공식 문서를 읽어보고 따라 하면서 진행해 봤지만 최근 일어난 사태로 인한 오류인지? 아니면 내가 값을 잘못 입력했는지? 키 쪽이 문제인지 여러 군데를 찾아보려고 노력했다. 오늘은 해결점을 찾지 못했다.

TIL 작성 전에 발견한 점이 있었다. 공식 문서에서 좌표계 이야기가 나왔고 WGS84 / KATEC라는 단어는 생소했지만 내가 넣으려는 값은 WGS84값이었던 거 같고 공식 예제 값은 KATEC 좌표계 값을 원하는 것 같다. 아! 느낌이 오는 거 같다. 또 변환해 줘야 하는구나… 내일 해결해 보려고 시도할 거 같다.

# 오늘의 코드 ⌨️

```swift
//https://school.programmers.co.kr/learn/courses/30/lessons/120826
return  my_string.components(separatedBy: letter).joined()
//components을 사용법을 알게 되었고 [String] 배열을 합치는 방법은 배열 타입의 메서드 중에 joined() 사용하는 것이 괜찮다고 느꼈다

//https://school.programmers.co.kr/learn/courses/30/lessons/120911
return ( String(my_string.lowercased().sorted()))
// my_string.lowercased()부분이 입력받은 값을 소문자로 변환시켜 스트링 값으로 변환합니다.
// .sorted()을 사용하면 정렬이 됩니다. 반환값은 요소 하나씩 [String]으로 변환되어 앞에 String( )으로 변환시켜주었습니다
```