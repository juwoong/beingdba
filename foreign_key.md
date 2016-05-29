# FOREIGN KEY 조건

다른 테이블의 **PRIMARY KEY**만 내용으로 쓸 수 있게 제한해주는 조건. 

`prof` table

|column|type|비고|
|:-:|:-:|:-:|
|_id|INTEGER|PRIMARY KEY|
|name|VARCHAR(32)|NOT NULL|

인 테이블의 id를 외래 키로 지정하려고 하면 다음과 같이 지정하면 된다.

```sql
CREATE TABLE student (
    _id INT(4) NOT NULL PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(32) NOT NULL,
    prof_id INT(4) NOT NULL,
    
    FOREIGN KEY (prof_id) REFERENCES prof (_id)
)
```
일반화하면 다음과 같다.

```sql
FOREIGN KEY (column_name) REFERENCES ref_table_name (ref_column_name);
```

만약, 위의 예시처럼, 학생이 있는 상태에서 선생님의 정보를 지우려고 한다면 다음과 같은 오류가 발생한다.

```
#1451 - Cannot delete or update a parent row:
a foreign key constraint fails (`test`.`student`, CONSTRAINT `emp_ibfk_1` FOREIGN KEY (`dept_no`) REFERENCES `dept` (`dept_no`))
```