
# "9251"

made by Jaehyeok Choi

## Welcome to Jaehyeok's github!

## What is the problem?

![button](https://github.com/Choi-JaeHyeok-21500749/9251/blob/main/9251_pro.JPG)

## What Algorithm should I use?

dynamic programming

## What was the key point and the hard part?

LCS is saving the maximum common seqeunce length in n * m array.

For example, ABCC ABCD can be like this.

0 0 A B C D

0 0 0 0 0 0

A 0 1 

B 0

C 0

C 0

add 0 in the front of each string and set the dp[i][j] value as 0. This is because we are using [i-1][j-1] value and we don't want to write extra if ,else code.

The reason why 1 appear is that ABCC's A and ACCD's A is same. It means we have one common character. 

It is like compare string "A" and string "A".

0 0 A B C D

0 0 0 0 0 0

A 0 1 1

B 0

C 0

C 0

Another 1 appeared. That is the situation that find LCS in string "AB" and "A". B and A is not same, but in comparing string "A" and string "A" case, we alreay found 1 common character, so write 1.

0 0 A B C D

0 0 0 0 0 0

A 0 1 1 1 1

B 0 1 2 

C 0

C 0

In here, comparing string "A" and "ABCC" end. Next, we will compare "AB" with "A" "AB" "ABC" "ABCD"

While doing that we compare "AB" and "AB". We found "B" as we common char. So we add one value to "A" "A" comparing case. 

This is because adding one char after "A" "A" will make "AB" "AB", not adding "AB" "A" case or "A" "AB".

0 0 A B C D

0 0 0 0 0 0

A 0 1 1 1 1

B 0 1 2 2 2

C 0 1 2 3 3

C 0 1 2 3 3

If two words does not match, find max(dp[i-1][j] , dp[i][j-1]) and fill dp[i][j].

This is because we are saving the maximum number in the dp.

The LCS of two string(string 1's length = n , string 2's length = m) will be dp[n-1][m-1].


## Where can I get more help, if I need it?

You can contact me through email, which is 21500749@handong.edu.
Thank you for visiting this github!

