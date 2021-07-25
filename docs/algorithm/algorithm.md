# 算法题

> 这里会存放我在`leetcode`上刷的算法题

## 存档

- 2020.5.2

```java
// 11.盛水最多的容器
//leetcode submit region begin(Prohibit modification and deletion)
class Solution {
    public int maxArea(int[] height) {
       // 使用双指针
       // l -> 左指针， r -> 右指针
       // area = min(l,r) * (l - r)
        int l = 0;
        int r = height.length - 1;
        int ans = 0;
        while (l < r)
        {
            int area = Math.min(height[l],height[r]) * (r - l);
            ans = Math.max(ans,area);
            if (height[l] <= height[r])
            {
                ++l;
            }
            else
            {
                --r;
            }
        }
        return ans;
    }
}
//leetcode submit region end(Prohibit modification and deletion)
```



