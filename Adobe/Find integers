class Solution {
public:
    vector <int> dp;
    int fun(int n) {
        if (n <= 2) return n+1;
        if (n == 3) return 3;
        int b = log2(n);
        int ans = dp[b];
        b--;
        if (n & (1<<b))
        return ans + dp[b];
        n = n & ((1<<b) - 1);
        return ans + fun(n);
    }
    int findIntegers(int n) {
        dp.resize(35, 0);
        dp[1] = 2;
        dp[2] = 3;
        for (int i=3;i<35;i++)
        dp[i] = dp[i-1] + dp[i-2];
        return fun(n);
    }
};
