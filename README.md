# post-javascript-study
* 간단히 url 을 통한 게시판 만들기
* 실행
  * $ npx parcel index.html

# study 내용
## HTML 
* shrink-to-fit=no : 브라우저 크기에 맞게 축소되어 조절되는 것을 막아줌 (특히 iOS / safari)
* Tailwind CSS : 유틸리티 클래스 기반의 CSS 프레임워크 => 사용자 정의 디자인을 빠르게 구현 가능
* crossorigin="anonymous" : 요청에 사용자의 자격 증명(쿠키, HTTP 인증)을 포함하지 않음 => 외부 리소스를 안전하게 로드하기 위해 사용 (ex. CDN)
* type="module" : 스크립트가 JavaScript 모듈임을 나타냄 / 모듈은 비동기로 로드되므로, 페이지의 다른 요소가 먼저 렌더링될 수 있음
* Font Awesome : 벡터 아이콘 및 로고를 제공하는 웹 폰트 및 CSS 프레임워크

## javascript
* AJAX(Asynchronous JavaScript And XML) : 비동기적으로 서버와 브라우저가 데이터를 교환할 수 있는 기술
  * XMLHttpRequest 객체를 사용하여 서버로부터 데이터를 받아오는 것
  * fetch API를 사용하여 AJAX 요청을 보내고 응답을 처리
* location : 현재 URL에 대한 정보를 제공하는 객체
  * location.href : 현재 URL을 문자열로 반환
  * location.hash : URL의 해시 문자열을 반환 => 해시 부분은 # 기호와 그 뒤에 오는 문자열로 구성 (ex. '#/page/1')
* addEventListener : 이벤트 핸들러를 등록하는 메서드 
  * hashchange : URL의 해시 부분이 변경될 때 발생하는 이벤트
* window.addEventListener('hashchange', router);
  * hashchange 이벤트가 발생하면 router 함수를 호출
* routePath.indexOf('#/page/') >= 0 : routePath 문자열에 '#/page/' 문자열이 포함되어 있는지 확인 
  * 포함되어 있다면 해당 문자열의 인덱스를 반환하고, 그렇지 않다면 -1을 반환

## common
* CDNJS(Content Delivery Network for JavaScript): 무료로 사용할 수 있는 오픈 소스 자바스크립트 라이브러리들을 제공하는 CDN 서비스 
  * CDN 서버는 전 세계에 분산되어 있어 사용자가 가장 가까운 서버에서 리소스를 다운로드
  * 로드 시간을 단축
  * 라이브러리를 호스팅할 필요가 없음
* git add 전체 취소 : git reset HEAD
* git add 취소 : git reset HEAD <file>
