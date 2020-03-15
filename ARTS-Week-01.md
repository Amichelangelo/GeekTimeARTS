## Algorithm
    LeetCode 两数之和      
    暴力求解法
```
    public static int[] TwoSum(int[] nums, int target)
        {
            Dictionary<int, int> numsDic = new Dictionary<int, int>();
            for (var i = 0; i < nums.Length; i++)
            {
                var num2 = target - nums[i];
                if (numsDic.ContainsKey(num2) && i != numsDic[num2])
                    return new[] { i, numsDic[num2] };
                if(!numsDic.Contains(nums[i]))
                    numsDic.Add(nums[i], i);
            }
            return null;
        }
```
## Review
    在看PythonCrashCourse第二版，翻译了目录和序言，本书包含基础知识和三个实战项目  
    https://github.com/Amichelangelo/Translate.git
## Tip
    C# 7.0 新特性，_用于丢弃（discard），如_=GetMoney()，代表不适用返回值，直接丢弃
    Markdown换行需要加两个空格
## Share
    暂无思路
