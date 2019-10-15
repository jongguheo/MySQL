## binlog_row_image

binary log가 row 포맷일 때, 갱신 내용을 바이너리 로그에 어떻게 기록할 것인지 설정하는 시스템 변수이다.

종류는 3가지가 있다.
- full 
- minimal 
- noblob 

full은 모든 컬럼을 기록하는 방식.

minimal은 변경된 컬럼만 기록하는 방식.

noblob은 BLOB이나 TEXT같은 타입을 제외한 컬럼을 기록하는 방식.

minimal이나 noblob을 사용하는 데 있어서 주의할 점이 있다.

마스터와 슬레이브 간의 테이블(컬럼 타입, 컬럼 순서, PK)이 동일해야 한다.

refer: https://dev.mysql.com/doc/refman/5.7/en/replication-options-binary-log.html#sysvar_binlog_row_image
