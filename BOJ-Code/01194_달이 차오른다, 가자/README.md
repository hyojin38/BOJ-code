# [BOJ] 01194 달이 차오른다, 가자.

### 문제 바로가기

>  https://www.acmicpc.net/problem/1194

### 알고리즘

> 그래프 이론. 그래프 탐색. BFS. 비트마스킹

### 문제 풀이 및 주의

>#### 1.중복 방문 가능한 BFS
>
>3차원 visited 로 해당 키를 가지고 있을때의 중복 방문 체크
>
>visited[][][][][][][][][][][ 51 ] [ 51 ] [ 64] 로 선언
>
>#### 2. 비트마스킹
>
>000001 : a
>
>000010 : b
>
>000100 : c
>
>​         :
>
>100000: f 
>
>모두 가진경우 111111 이므로 위 중복 방문 체크 에서 범위가 64가 된ek.

>[key 만들기]
>
>1 << 0  =>  1  000001
>
>1 << 1  =>  2  000010
>
>1 << 2  =>  4  000100
>
>1 << 3  =>  8  001000
>
>1 << 4  =>  16 010000
>
>1 << 5 => 32  100000
>
>1 << ch - 'a'
>
>newkey = (1 << ch- 'a' )  | key
>
>key |=  (1 << ch- 'a' )

> [key 확인하기]
>
>   000010   >> 확인하려는 키  (B 키)       1 << (door - 'A')
>
> &100111  >> 가지고 있는 키 (curkey)   curkey
>
> --------------
>
>   000010       000000  
>
>   000001
>
>   000100
>
> ​    있을때       없을때     => 따라서  0이면 없는것 



>#### 3. 구조체
>
>```c++
>struct 구조체명 {
>	int x,y,cnt,key;
>}; //구조체 선언
>vector < 구조체명 > V; // 벡터 활용 가능
>```