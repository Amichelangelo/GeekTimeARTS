ARTS
## Algorithm
LeetCode 02 两数相加
```
    // Definition for singly-linked list.
    public class ListNode
    {
        public int val;
        public ListNode next;
        private ListNode P;
        public ListNode(int x)
        {
            val = x;
        }
        
        // 通过构造函数赋值
        public ListNode(int[] xs)
        {
            P = new ListNode(0);
            val = xs[0];
            next = P;
            var xx = new int[xs.Length - 1];
            Array.Copy(xs,1,xx,0,xx.Length);
            foreach (var i in xx)
            {
                P.val = i;
                P.next = new ListNode(0);
                P = P.next;
            }
        }
    }

    // 解决过程 
    public static class Solution
    {
        public static ListNode AddTwoNumbers(ListNode l1, ListNode l2)
        {
            var result = new ListNode(0);
            var current = result;
            var val = 0;
            while (l1 != null || l2 != null || val!=0)
            {
                val +=(l1?.val??0) + (l2?.val??0);
                current.next = new ListNode(val > 9 ? val % 10 : val);
                current = current.next;
                val /= 10;
                l1 = l1?.next;
                l2 = l2?.next;
            }
            return result;
        }
    }
```

## Review

## Tip
MarkDown插入图片
* \![Alt text]\(图片链接 "optional title")
      图片链接：可以是图片的本地地址或者是网址。"optional title"：鼠标悬置于图片上会出现的标题文字，可以不写。
* \![avatar]\(图片链接) 
    图片链接：可以是图片的本地地址或者是网址，也可以是图片的base64字符串
    比如：
    ![avatar][base64str]
    [base64str]:data:image/png;base64,iVBORw0......

## Share
### C# 引用类型
* 引用类型存储对其数据（对象）的引用，同一数据能被多个变量引用；
* 操作一个引用类型的变量的值时，改变了被引用的的数据，其他变量受影响；
* 为引用类型的变量重新赋值时，改变的是该变量引用的目标，其他变量不受影响。
重新赋值 操作内容
![avatar](https://gitee.com/creatfororm/MarkDownGallery/raw/master/C%23/C%23%20Reference%20SimpleCode.png)
