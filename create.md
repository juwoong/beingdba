# CREATE 구문
**데이터베이스**를 만드는 작업과 **테이블**을 만드는 작업으로 나뉜다. 

####데이터베이스 만들기
```sql
CREATE DATABASE db_name;
```
데이터베이스는 이렇게 만든다. 손가락이 있으면 누구나 할 수 있다. 주의할  점은 MySQL의 기본 인코딩이 Latin1이라 한글이 안된다는 점인데, 데이터베이스를 만들 때 DB의 인코딩을 바꾸어 줄 수 있다.

```sql
CREATE DATABASE db_name CHARACTER SET utf-8
```

####테이블 만들기
테이블은 데이터베이스 안에서, 즉 DB를 사용중인 상태에서만 만들 수 있다. DB를 사용하는 방법은 다음과 같다.

```sql
USE database_name;
```

이제 테이블을 만들면 된다. 다음과 같은 구문이다.

```sql
CREATE TABLE table_name (
	column_name data_type(size) other options,
	column_name data_type(size) other options,
	...
)
```
**컬럼 이름**과 **데이터 타입**은 필수이며, 나머지 세팅은 부가적으로 쓸 수 있다. 가장 자주 쓰는 옵션은 **NOT NULL**
, **AUTO_INCREMENT**, **PRIMARY KEY** 등이 있겠다.

이에 관한 내용은 다음 챕터에서 자세하게 다루겠다.
