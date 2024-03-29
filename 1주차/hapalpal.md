

# GET
- 데이터를 URL의 쿼리 문자열에 첨부하여 전송
- 사용자가 서버에 데이터를 보내기 위해 URL을 호출할 때 사용됨.
- URL에 데이터가 노출되므로 보안에 취약함.
- 주로 서버로부터 데이터를 요청하고 가져올 때 사용. ex)검색요청 , 웹 페이지에 데이터 표시.
- 캐시 될 수 있음.

# POST
- 데이터를 body에 포함하여 전송.
- URL에 데이터가 노출되지 않아서 기뵤적 안전.
- 대량의 데이터를 전송할 수 있음.
- 전달된 데이터로 신규 리소스 등록, 프로세스 처리에 사용.
- 캐시 될 수 없음.

# 차이점 

1.보안
- GET은 URL에 데이터 일부가 포함되어 있기 때문에 보안성이 낮음. 반면 POST는 매개변수가 웹 서버 로그나 브라우저 히스토리에 저장되지 않기 때문에 비교적 안전함.

2.캐시
- GET 요청은 캐시될 수 있고 브라우저 히스토리에 남아있을 수 있음, 반면 POST 요청은 그렇지 않다. GET 요청은 북마크되고 공유되며 다시 방문할 수 있지만, POST 요청은 그렇지 않음.

3.서버측에 영향
- GET 요청은 데이터를 검색하기 위해 사용되며, 서버에 영향을 주지 않음. POST는 데이터를 서버로 보내 처리하기 때문에 데이터나 세션의 상태가 변경될 여지가 있음.

3.전송되는 데이터의 양
- GET은 최대 문자 수 제한이 있음. POST는 그러한 제한이 없음. GET 방식이 데이터를 리소스 URL을 통해 전송하는 반면 POST 방식은 body를 통해 전송하기 때문.

4.데이터 유형
- GET은 문자열 데이터만 지원. POST는 문자열, 숫자, 이진 데이터 등 다양한 데이터 유형을 지원.


