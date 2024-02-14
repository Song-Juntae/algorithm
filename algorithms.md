# 알고리즘

## 소수 판정법

    # 소수 정의에 따른 소수 판별법
    def isprime(N):
        for i in range(2, N):
            if N % i == 0:
                return False
        return True

Proof by Contradiction : (귀류법) 명제가 거짓이라고 가정하는 것이 모순으로 이어진다는 것을 보여주는 것으로 명제를 증명하는 방법.

명제, 모든 합성수는 2이상 자신의 제곱근 이하의 정수로 반드시 나누어 진다.

$$Proof.\,N이\,합성수고,\,1을\,제외한\,N의\,최소\,약수\,A가\,\sqrt{N}보다\,크다고\,가정해보자.$$

$$약수의\,성질로\,인해서\,A \times B = N이\,되는\,양의\,정수\,B가\,존재해야\,한다.\,이때\,B는\,N의\,약수다.$$

$$하지만\,B=N/A<\sqrt{N}이다.\,이는\,2이상의\,최소\,약수가\,A라는\,것과\,모순된다.$$

$$가정이\,성립되지\,않으므로\,명제는\,참이다.$$

    # 합성수 성질에 따른 소수 판별법
    def isprime(N):
        LIMIT = int(N ** 0.5)
        for i in range(2, LIMIT + 1):
            if N % i == 0:
            return False
        return True

## 약수 구하기

    # 합성수 성질에 따른 모든 약수 구하기
    def divisors(N):
        divs = []
        LIMIT = int(N ** 0.5)
        for i in range(2, LIMIT + 1):
            if N % i == 0:
                divs.append(i)
                if i != N // i:
                    divs.append(N//i)
        return sorted(divs)

## 소인수 분해

    # 합성수 성질에 따른 소인수 분해하기
    def prime_factors(N):
        p_factors = []
        LIMIT = int(N ** 0.5)
        for i in range(2, LIMIT + 1):
            while N % i == 0:
                N /= i
                p_factors.append(i)
        if N >= 2:
            p_factors.append(int(N))
        return p_factors
