# [BOJ] 9372 상근이의 여행

### 문제 바로가기

>  https://www.acmicpc.net/problem/9372

### 알고리즘

> - [그래프 이론](https://www.acmicpc.net/problem/tag/7)
> - [트리](https://www.acmicpc.net/problem/tag/120)

### 문제 풀이 및 주의

> 상근이가 모든 국가를 여행하기위해 타야하는 비행기 종류의 최소 개수를 출력하기

#### [ MST의 간선의 수 항상 N-1]

> **여러 비행기를 통해 모든 국가를 연결할 수 있을때, 모든 국가를 지나도록 이용할 수 있는 최소 비행기의 갯수는 국가갯수 -1 이다**
>
> 의 개념을 활용 (주어지는 비행 스케줄은 항상 연결 그래프를 이루기 때문)

