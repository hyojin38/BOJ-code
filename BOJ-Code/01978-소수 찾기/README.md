# [BOJ]  1978 소수 찾기

### 문제 바로가기

>  https://www.acmicpc.net/problem/1978

### 알고리즘

> 수학. 정수론. 소수 판정, 에라토스테네스의 체

### 문제 풀이 및 주의

>#### 소수:Prime Number
>
>소수는 자신보다 작은 두개의 자연수를 곱하여 만들 수 없는 1 보다 큰 자연수이다.
>
>ex) 7는 7 * 1 또는 1 * 7로 수를 곱합 결과를 적는 유일한 방법이 그 수 자신을 포함하기 때문에 소수이다.

> #### 소수 판별 알고리즘
>
> 기본적으로 소수를 판별하는 방법은 어느 수까지 판별하는 수를 나눠서 나머지가 0이 나오면 소수로 인정한다.

> #### 방법 1
>
> 2부터 판별하는 수 전까지 나눠보고 나머지가 0이 안나온다면 소수로 정의한다.
>
> 해당 판별하는 수 까지 모두 확인해야하므로 시간 복잡도는 0(N)으로 가장 기본적인 방법이다

>#### 방법 2
>
>해당 숫자의 절반까지 확인하여 나머지가 0이 나오지않는다면 소수로 정의한다.
>
>절반 이상의 숫자는 확인이 필요없는 숫지이기 때문에 가능하다.
>
>자기 자신을 제외하고 절반을 초과하는 숫자에서 나눴을때 나머지가 0이 되는 숫자는 나올 수 없다
>
>시간 복잡도  O(N)

> #### 방법 3_ 소수 판별 가장 효율적 방법
>
> 해당 숫자의 **√N** 까지 확인 하기. 이 원리는 약수의 중심을 구하는 방법이다. 
>
> 예를 들어 80의 약수는 1.2.4.5.8.10.16.20.40.80 이다
>
> **1:80, 2:40, 4:20, 5:16, 8:10**. √80의 값은 대략 8.xxx의 값이 나온다. 
>
> 즉 약수들의 곱으로 봤을때 루트를 씌운 값이 중간값이 된다.
>
> 이 원리를 이용하여 2에서부터 √N 의 값까지 검색을한다며 이후의 값은 확인할 필요가 없다.
>
>  시간 복잡도  O(√N)
>
> ```c++
>   bool isPrime(int num){
>         for(int i=2; i*i<=num; i++){//제곱근 활용
>             if(num % i == 0) return false;
>         }
>         return true;
>     }
> ```
>
> 