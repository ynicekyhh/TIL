### 오라클 6.x버전에서 사용자 권한 설정

1. conn /as sysdba

2. create user jblog identified by jblog;

3. grant connect, resource to jblog;


###### SQL
- DDL(DA) : table만들기, 요즘엔 툴을 사용
- DCL + Data Modeling(DBA) : 권한설정
- DML(개발자) : 쿼리문
