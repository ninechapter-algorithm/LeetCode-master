## [leetcode/lintcode 题解] 谷歌面试题：猜数字游戏

### 描述

你正在和你的朋友玩 猜数字 (Bulls and Cows)游戏：你写下一个数字让你的朋友猜。每次他猜测后，你给他一个提示，告诉他有多少位数字和确切位置都猜对了（称为“Bulls”, 公牛），有多少位数字猜对了但是位置不对（称为“Cows”, 奶牛）。你的朋友将会根据提示继续猜，直到猜出秘密数字。
请写出一个根据秘密数字和朋友的猜测数返回提示的函数，用 A 表示公牛，用 B 表示奶牛。
请注意秘密数字和朋友的猜测数都可能含有重复数字。
你可以假设秘密数字和朋友的猜测数都只包含数字，并且它们的长度永远相等
[在线评测地址](https://www.lintcode.com/problem/1299/?utm_source=sc-github-sy)

### 样例1

```
输入：secret = "1807", guess = "7810"
输出："1A3B"
解释：1 公牛和 3 奶牛。公牛是 8，奶牛是 0, 1 和 7。
```

### 样例 2

```
输入：secret = "1123", guess = "0111"
输出："1A1B"
解释：朋友猜测数中的第一个 1 是公牛，第二个或第三个 1 可被视为奶牛。
```

### 解题思路

### 考点：哈希表

### 题解：第一遍遍历计算所有相同位置大小相同的个数，分别用大小为10的数组记录两个字符串每个数字出现的次数，第二次遍历数组，相同的次数为对应位置的最小值。

### 源代码

```
class Solution {
    public String getHint(String secret, String guess) {
        int a = 0,b = 0, n = secret.length();
        int[] ds = new int[10];
        int[] dg = new int[10];
        for(int i = 0; i < n; i++){
            int x = secret.charAt(i)-'0';
            int y = guess.charAt(i)-'0';
            if(x == y) {
                a++;
            }
            ds[x]++;
            dg[y]++;
        }
        for(int i = 0; i < 10; i++) {
            b += Math.min(ds[i],dg[i]);
        }
        return a+""+'A'+(b-a)+""+'B';
    }
}
```

[更多题解参考](https://www.jiuzhang.com/solution/bulls-and-cows/?utm_source=sc-github-sy)
