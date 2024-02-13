# 알고리즘

## 소수 판정법

    # 소수 정의에 따른 소수 판별법
    def isprime(N):
        for i in range(2, N):
            if N % i == 0:
                return False
        return True
        
모든 합성수는 2이상 자신의 제곱근 이하의 정수로 반드시 나누어 진다.

$$ 증명 \, pf) \, N을 \, 합성수라고 \, 하면, \, N=AB, \, 1< A,B < N 이다. $$
$$ 만약 \, A < B \, 이고, \, A > \sqrt{N} \, 이라면, $$
$$ B = N / A < A \, 이므로 \, 모순이다. $$

    # 합성수 성질에 따른 소수 판별법
    def isprime(N):
        LIMIT = int(N ** 0.5)
        for i in range(2, LIMIT + 1):
            if N % i == 0:
            return False
        return True
