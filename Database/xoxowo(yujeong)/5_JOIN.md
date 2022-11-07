## 조인 (JOIN)
    하나의 테이블이 아닌 **두개 이상의 테이블을 묶어서** 하나의 결과물로 만드는 것.
    MySQL에서는 JOIN이라는 쿼리로 MongoDB에서는 lookup이라는 쿼리로 처리한다.

* 참고로 MongoDB는 성능이 떨어지기 때문에 lookup을 되도록 지양해야한다. 그래서 여러 테이블을 JOIN하는 작업이 많을 수록 관계형데이터베이스를 사용해야한다.

### 조인의 종류
    조인은 두개 이상의 테이블을 묶어 하나의 결과물로 만드는 것이기 때문에 여러가지 조인이 있는데, 
    대표적으로 내부조인, 왼쪽 조인, 오른쪽 조인, 합집합 조인이 있다.

<img src="https://i.ibb.co/0skHY82/2022-02-24-6-58-10.png">

#### 내부조인 (inner join)
    내부 조인은 두 테이블 간의 **교집합**을 나타낸다.

```SQL
SELECT * FROM TableA A
INNER JOIN TableB B ON
A.key = B.key
```


#### 왼쪽 조인 (left outer join)
    왼쪽 조인은 테이블 B의 일치하는 부분의 레코드와 함께 테이블 A를 기준으로 완전한 코드 집합을 생성한다.
    만약 테이블 B에 일치하는 항목이 없으면 해당 값은 null 값이 된다.

```SQL
SELECT * FROM TableA A
LEFT JOIN TableB B ON
A.key = B.key
```


#### 오른쪽 조인 (right outer join)

#### 합집합 조인 (full outer join)