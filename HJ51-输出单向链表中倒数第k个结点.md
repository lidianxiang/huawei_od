## 1. 题目描述

输入一个单向链表，输出该链表中倒数第k个结点，链表的倒数第1个结点为链表的尾指针。

示例1:

```
输入：8
	 1 2 3 4 5 6 7 8
	 4
输出：5
```



## 2. Solution

```python
class ListNode:
    def __init__(self, x):
        self.val = x
        self.next = None
        
        
while True:
    try:
        head = ListNode(-1)
        count, num_list, k = int(input()), list(map(int, input().split())), int(input())
        while k:
            head.next = ListNode(num_list.pop())
            head = head.next 
            k -= 1
        print(head.val)
    except:
        break
```

