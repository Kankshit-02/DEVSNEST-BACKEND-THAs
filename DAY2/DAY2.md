## DAY2 THA

1. postgres=# CREATE TABLE COMPANY(
    postgres(# ID INT PRIMARY KEY NOT NULL,
    postgres(# NAME TEXT NOT NULL,
    postgres(# AGE INT NOT NULL,
    postgres(# ADDRESS CHAR(50),
    postgres(# SALARY REAL)
    postgres-# ;

2. postgres=# \d COMPANY
                  Table "public.company"
    Column  |      Type      | Collation | Nullable | Default
    ---------+----------------+-----------+----------+---------
    id      | integer        |           | not null |
     name    | text           |           | not null |
    age     | integer        |           | not null |
    address | character(1)[] |           |          |
     salary  | real           |           |          |
    Indexes:
        "company_pkey" PRIMARY KEY, btree (id)

3. postgres=# CREATE TABLE DEPARTMENT(
    postgres(# ID INT PRIMARY KEY NOT NULL,
    postgres(# DEPT CHAR[50] NOT NULL,
    postgres(# EMP_ID INT NOT NULL);

4. postgres=# CREATE SCHEMA mySchema;
    CREATE SCHEMA
    postgres=# CREATE TABLE mySchema.company(
    postgres(# ID INT NOT NULL,
    postgres(# NAME VARCHAR[20] NOT NULL,
    postgres(# AGE INT NOT NULL,
    postgres(# ADDRESS CHAR[25],
    postgres(# SALARY DECIMAL(18,2),
    postgres(# PRIMARY KEY(ID)
    postgres(# );

5. postgres=# DROP SCHEMA mySchema;

6. postgres=# INSERT INTO COMPANY(ID,NAME,AGE,ADDRESS,SALARY,JOIN_DATE) VALUES (1,'KANKSHIT',18,'NAGPUR',  6000.00,'2009-01-01');

7. postgres=# SELECT (15*2) AS ADDITION;
    
    postgres=# SELECT COUNT(*) FROM COMPANY;
     count
    -------
         1
    (1 row)

    postgres=# SELECT COUNT(*) AS "RECORDS" FROM COMPANY;
    RECORDS
    ---------
        1
    (1 row)

    postgres=# SELECT CURRENT_TIMESTAMP AS TIME;
                time
    ----------------------------------
    2021-09-20 14:16:45.461539+05:30
    (1 row)

8. postgres=# SELECT * FROM COMPANY WHERE SALARY>5000;
    postgres=# SELECT * FROM COMPANY WHERE NAME LIKE 'K%';
    postgres=# SELECT * FROM COMPANY WHERE NAME LIKE 'K_______';
    postgres=# SELECT * FROM COMPANY WHERE NAME LIKE '_A%';
    postgres=# SELECT * FROM COMPANY WHERE AGE BETWEEN 5 AND 10;
    postgres=# SELECT * FROM COMPANY WHERE AGE IN (10,20);

9. postgres=# UPDATE COMPANY SET AGE=60,NAME='JIMMY' WHERE ID=3;
    postgres=# DELETE FROM COMPANY WHERE ID=2;

10. postgres=# CREATE TABLE CUSTOMERS(
    postgres(# CUST_ID INT GENERATED ALWAYS AS IDENTITY,
    postgres(# CUST_NAME VARCHAR(30) NOT NULL,
    postgres(# PRIMARY KEY(CUST_ID));

11. postgres=# CREATE TABLE CONTACTS(
    CONTACT_ID INT NOT NULL ,
    CUST_ID INT,
    CONTACT_NAME VARCHAR(200) NOT NULL,
    PHONE VARCHAR(15),
    EMAIL VARCHAR(100),
    PRIMARY KEY(CONTACT_ID),
    CONSTRAINT FK_CUSTOMER
    FOREIGN KEY(CUST_ID) REFERENCES CUSTOMERS(CUST_ID) ON DELETE CASCADE);