# algorithm

## 자료구조

* 정의 : 데이터에 효율적으로 접근하고 수정할 수 있도록 저장, 조직, 관리하는 방법

* 관계 : 이산수학, ADT(Abstract data type), 알고리즘

* 종류 : 배열, 연결리스트, 행렬, 스택, 큐, 그래프, 트리, 힙

## 알고리즘

* 정의 : 문제를 해결하는 절차
* 관계 : 이산수학, 자료구조, 알고리즘 패러다임
* 종류 : 
	* 전체 탐색, 이진 탐색, 조합 전체 탐색
	* 소수 판정법, 수열 나열, 유클리드 호제법, 몬테카를로법, 선택 정렬, 재귀 함수, 분할 정복법, 병합 정렬, 동적계획법, 배열 이진 탐색
	* 계산 기하, 누적합, 뉴턴법, 에라토스테네스의 체, 깊이 우선 탐색, 너비 우선 탐색, 반복 제곱법, 행렬 거듭제곱, 경사 하강법,
	* 탐욕법, A*


## 알고리즘 패러다임

알고리즘 패러다임 또는 알고리즘 설계 패러다임은 알고리즘 클래스의 설계의 기초가 되는 일반 모델 또는 프레임워크입니다. 
알고리즘 패러다임은 알고리즘이 컴퓨터 프로그램보다 높은 추상화인 것처럼 알고리즘의 개념보다 높은 추상화입니다.

* General
	* Backtracking
	* Branch and bound
	* Brute-force search
	* Divide and conquer
	* Dynamic programming
	* Greedy algorithm
	* Recursion
	* Prune and search
* Parameterized complexity
	* Kernelization
	* Iterative compression
* Computational geometry
	* Sweep line algorithms
	* Rotating calipers
	* Randomized incremental construction

1. 알고리즘 설계 기법 (패러다임) / 문제 해결 접근 전략 (Algorithm Design Paradigm)

ㅇ 문제를 해결하는 과정에서, 
	- 어떤 전략과 접근방식으로, 그 해법을 찾아가야 하는지에 대한,
	- 다양한 방법론/해결법들을 다룸

ㅇ 주요 분류
	- 무작위 대입 기법 (Brute Force Technique)
	- 분할 정복법
	- 욕심쟁이 방법
	- 동적 계획법
	- 백트래킹 등

ㅇ 문제를 풀 때, 위 각각의 방법론(전략)에 따라,
	- 저마다 달리 문제를 푸는 독특한 해결 단계/절차를 알고리즘 이라고 함


2. 무작위 대입 기법, 억지 기법 (Brute Force Technique)

ㅇ 단순하고 고지식하지만, 광범위한 문제에 적용 가능한 알고리즘 설계 기법
	- 입력 크기가 작은 경우, 오히려 충분히 빠를 수 있음
	- 타 효율적인 알고리즘 설계 및 분석의 이론적 기반이 됨


3. 분할 정복/분할 통치 (Divide and Conquer) 전략

ㅇ 풀이 방식
	- 문제를 작은 문제로 나눠 순환적으로 푸는 하향식 접근 방식
	- 다만, 문제의 해를 구할 때는 상향적으로 구해짐
	- 결국, 각 순환 마다, 분할,정복,결합의 단계를 거침

ㅇ 적용 例)
	- 이진 탐색, 퀵 정렬, 합병 정렬
	- 선택 문제 (최대값/최소값 찾기, n번째 작은 원소 찾기 문제 등)
	- 선형 시스템 풀기, 함수의 근 찾기, 보간법, 수치 적분 등


4. 동적 계획법 (Dynamic Programming, 다이내믹 프로그래밍) 전략

ㅇ 풀이 방식
	- 아래에서 위로 해결하면서 전체 문제를 해결하는 상향식 접근 방식
	. 간단한 하위 문제부터 해결하면서,
	. 하위 문제의 해를 테이블에 저장해 놓고,
	. 이를 이용하여, 좀더 복잡한 상위 문제를 해결하여 나아감

ㅇ 적용 例) 최단경로 알고리즘 (플로이드 알고리즘, 벨만 포드 알고리즘) 등


5. 탐욕 알고리즘 (Greedy Algorithm) 전략 

ㅇ 풀이 방식
	- 그때그때 가장좋은 해결핵을 찾아가는 기법
	. 해를 구하는 일련의 선택 과정 마다,
	. 가장 좋아보이는 최선을 선택하면, 전체적으로 최적 해를 구할 수 있다는 방법론으로,
	. 각 단계 마다 최상으로 보이는 해결책으로 구한 해들을 모아 제시하게 됨

ㅇ 적용 例)
	- 동전 거스름돈을 가장 적은 수의 동전으로 주는 문제 
	- 최단경로 알고리즘 (다익스트라 알고리즘)
	- 최소비용 신장트리를 구하는 알고리즘 (크루스칼 알고리즘, 프림 알고리즘) 등


6. 백트래킹 (Backtracking, 되추적) 방법

ㅇ 문제 풀이의 막다른 곳에 다다르면, 호출한 함수로 되돌려 나아가는 방법 
	- 더이상 해가 없으면 왔던 길을 되돌아가서 다른 길을 찾아보는 방법
	- 문제를 푸는 과정 중 발생할 수 있는 모든 가능한 상태를 상태 공간 트리로써 구축함
	- 주로, 깊이우선탐색(Depth First Search) 알고리즘을 이용하여 해답을 찾게됨

ㅇ 특징
	- 해를 구할 때까지 모든 가능성을 시도 함
	- 갈 수 있는데까지 가보다가 막히면 (더이상 찾던 해가 없으면),
	. 되돌아와서 다른 길을 찾아봄
	- 되추적을 통해 탐색 대상을 줄여나감
	. 되추적이 발생하면, 해당 서브트리들은 탐색대상에서 제외됨
	- 주로, 그래프(상태 공간 트리)에 대해 DFS(깊이우선탐색)으로 탐색하며,
	. 재귀적으로 구현됨
	- 문제가 커질 경우 엄청난 시간이 걸리므로, 
	. 분기한정법(Branch-and-Bound) 등 탐색 범위를 줄이는 여러 보완을 취함

ㅇ 적용 例) 최적화 문제, 판정 문제 등


7. NP 문제 (NP, Nondeterministic Polynomial Problem), NP 완비 문제 (NP-complete)

ㅇ 아직까지, 다항식 시간 O(nk) 내에,
	- 해결 가능한 최적 알고리즘을 찾지 못하였으며,
	- 그같은 최적 알고리즘의 존재 여부도 증명을 못하는 경우가 있음
ㅇ 사실상, 꽤 많은 문제가 이같은 성질을 함께 갖음
ㅇ 그러나, 만일 이같은 문제들 중 하나라도 다항식 시간 O(nk) 내에,
	- 해결 가능한 알고리즘이 존재하면,
ㅇ 그렇다면, 나머지 모든 문제도,
	- 다항식 시간 O(nk) 내에 해결 가능 하다는, 논리적 연결 체계를 갖음
ㅇ 결국, 비결정론적 다항식 시간 내 해결 가능하다고, 확인할 수 있는 문제들을 말함

ㅇ 적용 例) 외판원 문제 (traveling-saleman problem, TSP 문제) 등

  