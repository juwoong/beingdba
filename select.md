# SELECT 구문
데이터베이스의 기본이 되는 I/O 작업 중 O를 담당한다.

```sql
SELECT column_name, ... FROM table_name
```

다음 형태가 기본이며, column name에는 가져오고 싶은 특정한 컬럼 이름을 넣는다. 만약 모든 컬럼을 다 가져오고 싶다면 다음과 column_name 대신 *을 하나 적어준다.

```sql
SELECT * FROM table_name
```

특정 튜플을 가지고 오고 싶은 경우는 SELECT 구문 이후에 WHERE로 조건문을 서술한다. 예를 들어, 학생번호 컬럼의 이름이 `studentId`이고, `3519`라는 학번을 가지고 오고 싶은 경우에는 다음과 같이 적어주면 된다.

```sql
SELECT * FROM students WHERE studentId = 3519
```

그것이 아니라, 학생의 이름만 가지고 오고 싶다면 다음과 같이 입력하면 된다.

```sql
SELECT name FROM students
```


