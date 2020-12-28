# 지역기반 경매시스템을 이용한 중고거래 플랫폼
### BootStrap / HTML / CSS / JavaScript / PHP / MYSQL(MariaDB)

http://themodern.pe.kr/capstone (본 페이지는 모바일에 최적화 되어있습니다.)
<br><br><br><br>
### 1. 프로젝트 개요
------------
현재, 언제 어디서나 온라인 플랫폼을 통해 물건을 확인하고 중고거래를 할 수 있다.하지만 중고거래 특성상 비싸게 판매하려는 판매자와 저렴한 가격에 구매하려는 구매자 간의 난처한 상황이 발생한다. 그리고 상품의 상태와 가격은 만족하지만 직거래 희망 시 지역이 너무 멀어 거래를 못하는 경우가 있다. 또한 거래 후 판매자는 환불 의무가 없지만, 구매자가 철저히 확인을 하지 않고 구매하여 사후 문제가 빈번하게 발생한다. 이러한 문제로 장기간 거래가 이루어지지 않는 거래품목이 너무 많은 것이 현 상황이다.<br><br>
<strong><u>  때문에, 사후 문제를 미연에 방지하고자 상품 상태 체크리스트 기능과 판매자와 구매자가 같이 가격을 만들어 나가는 경매 시스템을 도입하고, 지역기반 검색시스템을 통해 거래를 활성화 시킬 수 있는 플랫폼을 구현한다.<br><br><br>

### 2. 유스케이스 다이어그램
------------
![유스케이스 다이어그램](https://user-images.githubusercontent.com/75834395/102696883-00fb2d00-4275-11eb-9170-f95ce0579db2.jpg)
- Actor는 회원이 있으며 중고거래 상품 구매자와 판매자로 세분화되나 구매자가 판매자가 될 수도, 판매자가 구매자가 될 수도 있다.
- 구매자는 플랫폼에 등록된 중고 상품을 조회할 수 있으며, 상품 조회는 전체상품 목록 조회와 필요한 상품을 검색하는 상품 검색이 있다. 이에 대한 확장관계에 있는 상품상세조회를 통해 한 단계 더 확장관계에 있는 입찰, 체크리스트 확인, 판매자와 채팅이 가능하며 이를 통해 판매자의 물건을 구매할 수 있다.
- 판매자는 플랫폼에 중고 상품을 등록할 수 있으며, 내 정보관리의 확장 관계인 내가 쓴 글 목록 조회를 통해 한 단계 더 확장 관계에 있는 상품관리를 통해 상품 수정, 상품 삭제, 상품 상태 변경이 가능하다.
-구매자와 판매자 모두 내 정보 관리의 일반화 관계에 있는 회원정보 수정, 회원탈퇴, 로그아웃이 가능하며, 채팅목록조회를 통해 확장관계인 채팅하기를 할 수 있다. 이 모든 기능을 이용하기 위해선 회원가입과 로그인이 필수적이다.
<br><br><br>

### 3. 동작 구조
------------
![구현 구조](https://user-images.githubusercontent.com/75834395/103204437-b778a500-493a-11eb-9a0d-029d1a1cd76b.jpg)
<br><br><br>

### 4. 구현 화면
------------
![뉴1](https://user-images.githubusercontent.com/75834395/103206178-987c1200-493e-11eb-98a7-e3fd5431534a.jpg)
- <로그인 화면>은 접속 시 처음 출력되는 페이지이다. 로그인 실패 시 경고 창을 띄우고, 성공 시 메인 화면으로 넘어간다.
- <회원가입>에서 회원가입을 할 수 있다. 정보를 입력받아 DB에 저장한다.
- <메인화면>에서 로그인된 회원의 지역을 기반으로 최근 등록된 상품을 보여준다.
- <네비게이션>을 통해 홈, 상품등록, 채팅, 내정보, 상품 검색을 할 수 있다. 상품검색은 상품명으로 검색할 수 있다.
<br><br><br>
![뉴2](https://user-images.githubusercontent.com/75834395/103206179-99ad3f00-493e-11eb-9cd9-f9dffc4be134.jpg)
![3](https://user-images.githubusercontent.com/75834395/103170797-7fb22480-488a-11eb-81e3-737ed45e8ae0.jpg)
![4](https://user-images.githubusercontent.com/75834395/103170798-7fb22480-488a-11eb-88f1-03e2775c3eb1.jpg)
