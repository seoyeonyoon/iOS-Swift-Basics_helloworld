# 3. Interaction
이번 세션에서는 앞서 공부한 개발환경과 Swift언어를 이용해 간단한 예제를 만들어 보려 한다. 이번에 다룰 예제는 MoneyConverter라는 환전 앱이다.



## 3-1. View & Control
안녕, 링고스타 윤성관.
이번 시간에는 MoneyConverter의 UI를 구성해 보자.

### UI 구성
 * 세그먼티드 컨트롤 : 몇 개의 항목 중 하나를 선택해야 할 때. 주로 정렬 방식 정의.
 * 텍스트 필드 : 문자열 입력을 받는다. 다양한 키보드 종류.
 * 버튼 : 사용자의 이벤트를 받는 기본적인 UI 컨트롤. 상태값을 가지고 있다.
 * 레이블  : 문자열 표시를 위한 뷰 오브젝트. 여기서는 결과값을 표시할 것이다.

 
### Outlet 연결
인터페이스 빌더에서 만든 오브젝트들 중 코드를 통해 접근할 필요가 있는 모든 오브젝트들에 아울렛을 붙인다고 생각하자.

아울렛이 뭘까? 좀 다른 얘기지만. 콘센트. 아울렛. 연결 접점.
여기에서는 스토리보드로 만든 UI와 Swift 코드간의 연결 접점이라고 이해.


세그먼티드 컨트롤은 선택된 인덱스 값을 읽기 위해 , 텍스트 필드는 사용자 입력 값을 읽기 위해, 레이블은 결과값을 넣기 위해 필요.
버튼은 우리가 버튼의 상태를 읽거나 버튼의 레이블|이미지를 변경해야 하는 상황이 있다면 아울렛을 더해야 하지만 지금은 그렇지 않음.
 
### 액션 연결과 구현

버튼은 눌렀을 때 동작하는 액션 메소드 연결.
Swift 코드를 이용해, 세그먼티드 컨트롤의 값에 따라 환율을 정하고
텍스트 필드의 값을 읽어서 그게 정당한 숫자값이면 계산 결과를 표시한다.


## 3-2. MoneyClass 제작

 

---

절취선

---

## 버튼의 상태값 조정.
* 델리게이트 프로토콜 연결
* 텍스트 필드의 편집이 끝나면 값을 validation 한 뒤 변환 가능한 숫자값이 입력되었으면 버튼을 활성화 한다. 