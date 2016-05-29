# AUTO_INCREMENT 조건
**자동**_**증가**조건. 각 ROW가 추가될 때 마다, 값이 1씩 증가한다.

##예시
```sql
CREATE TABLE test (
    value int(11) not null auto_increment
);
```
인 테이블에 한줄 한줄 추가해보도록 하겠다.

```sql
INSERT INTO tast VALUES();
```

|value|
|:-:|
|1|

인 상태가 된다. 한번 더 구문을 날리면 다음과 같이 변한다.

|value|
|:-:|
|1|
|2|

구문을 3번 더 날리면 다음과 같이 변한다.

|value|
|:-:|
|1|
|2|
|3|
|4|
|5|

따로 쓰이기보단, 