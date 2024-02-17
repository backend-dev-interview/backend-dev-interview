# SQL - JOIN
 - 여러 테이블에서 가져온 레코드를 조합하여 하나의 테이블이나 결과 집합으로 표현해 주는 SQL 구문
## INNER JOIN
 - 표준 SQL과는 달리 MySQL에서는 JOIN, INNER JOIN, CROSS JOIN이 모두 같은 의미로 사용됨.
  ```SQL
select u.userid, name 
from usertbl as u inner join buytbl as b 
on u.userid=b.userid 
where u.userid="111" -- join을 완료하고 where조건을 수행.
```
## OUTER JOIN (LEFT , RIGHT , FULL)
 - OUTER JOIN은 조인하는 테이블의 ON 절의 조건 중 한쪽의 데이터를 모두 가져온다. 
  (왼쪽/오른쪽을 기준으로 했느냐에 따라 기준 테이블의 것은 모두 출력.)
- LEFT JOIN은 두 테이블이 있을 경우, 첫 번째 테이블을 기준으로 두 번째 테이블을 조합하는 JOIN.
```SQL
select u.userid, name 
from usertbl as u inner join buytbl as b 
on u.userid=b.userid 
where u.userid="111"  join을 완료하고 where조건을 수행.
```
- RIGHT JOIN은 두 테이블이 있을 경우, 두 번째 테이블을 기준으로 첫 번째 테이블을 조합하는 JOIN
```SQL
   -- 예) 1학년 학생의 이름과 지도교수명을 출력하라. 단, 지도교수가 지정되지 않은 학생도 출력되게 하라.

SELECT STUDENT.NAME, PROFESSOR.NAME 
FROM STUDENT RIGHT OUTER JOIN PROFESSOR -- PROFESSOR를 기준으로 오른쪽 조인
ON STUDENT.PID = PROFESSOR.ID 
WHERE GRADE = 1
```
- FULL OUTER JOIN은 성능상 거의 사용하지 않는다.
  
