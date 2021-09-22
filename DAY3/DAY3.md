1. redis-cli
2. SUBSCRIBE {channel name}
3. PSUBSCIRBE d*
4. PUBLISH devsnest hello
5. UNSUBSCRIBE {Channel name}
6.  1. XADD mystream 10000 name Anna
    2. XADD mystream 10001 name ROBERT
    3. XADD mystream * name Kankshit            {Random ID goes when *} {"1632216862183-0" here}
7. XREAD COUNT 200 STREAMS mystream 0
8. XREAD COUNT 200 STREAMS mystream 10002-0     {All entries after 10002-0}
9. XREAD BLOCK 0 STREAMS mystream 0
10. XREAD BLOCK 10000 STREAMS mystream $
11. XRANGE mystream - +  COUNT 3
12. XREVREANGE mystream + - COUNT 3