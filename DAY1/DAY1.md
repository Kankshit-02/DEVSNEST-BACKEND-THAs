## Day1 : SQL and REDIS Basics

### REDIS COMMANDS

1. redis-cli
2. {name: "Kankshit:,age: 18}
3. KEYS *
4. EXPIRE
5. SETEX

#### ARRAY AND SET
1. lpush
2. rpush
3. lrange
4. lpop
5. rpop
6. SADD
7. SMEMBERS

#### NESTING OBJECTS
1. HSET
2. HGETALL
3. HDEL
4. HEXISTS

### POSTGRES COMMANDS

1. psql -u postgres
2. CREATE USER devsnest WITH PASSWORD 'password';
3. CREATE DATABASE devs;
4. GRANT ALL PRIVILAGES ON DATABASE devs to devsnest;
5. \l {for list of all databases}
6. \c devs {Connect to the database devs}
7. CREATE TABLE COMPANY (ID INT NOT NULL,NAME CHAR[50],AGE INT, ADDRESS TEXT,);
