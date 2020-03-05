class Solution:
    def longestPalindrome(self, s: str) -> str:
        ans = ''
        max_len = 0
        n = len(s)
        dp = [[False]*n for _ in range(n)]
        for i in range(n):
            dp[i][i] = True
            max_len = 1
            ans = s[i]
            
        for i in range(n-1):
            if s[i] == s[i+1]:
                dp[i][i+1] = True
                ans = s[i:i+2]
                max_len = 2
                
        for j in range(n):
            for i in range(0,j-1):
                if s[i] == s[j] and dp[i+1][j-1]:
                    dp[i][j] = True
                    if max_len < j-i+1:
                        ans = s[i:j+1]
                        max_len = j-i+1
        return ans
