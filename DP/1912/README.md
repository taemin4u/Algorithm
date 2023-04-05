dp[n]에는 n번째까지 고려했을 때 연속 최대 값이 담겨있다.

dp[n+1]은 만약 dp[n]이 음수라면 dp[n] + arr[n+1]이 arr[n+1]보다 작을 것이고 arr[n+1]부터 다시 연속 합을 구하는 연산이 시작된다.

dp[n]이 양수라면 arr[n+1]을 더한 것이 여전히 더 크다.

즉 dp[n+1]은 다음과 같다.

> dp[n+1] = max(dp[n] + arr[n+1], arr[n+1])