## 1.题目描述

MP3 Player因为屏幕较小，显示歌曲列表的时候每屏只能显示几首歌曲，用户要通过上下键才能浏览所有的歌曲。为了简化处理，假设每屏只能显示4首歌曲，光标初始的位置为第1首歌。



现在要实现通过上下键控制光标移动来浏览歌曲列表，控制逻辑如下：

1. 歌曲总数<=4的时候，不需要翻页，只是挪动光标位置。

光标在第一首歌曲上时，按Up键光标挪到最后一首歌曲；光标在最后一首歌曲时，按Down键光标挪到第一首歌曲。

示例1:

```
输入：
    10
    UUUU
输出：
    7 8 9 10
    7
```



## 2. Solution

```python
mapping = {'U': -1, 'D': 1}

def run(n, seq):
    index = 0
    start, end = index, index+4
    
    for s in seq:
        index = index + mapping[s]
        if index < 0:
            index += n 
            start, end = max(n-4, 0), n 
        elif index >= n:
            index -= n 
            start, end = 0, 4
        if index < start:
            start -= 1
            end -= 1
        elif index >= end:
            start += 1
            end += 1
    window = list(range(start+1, end+1))
    return window, index+1

n = int(input())
seq = input().strip()
a, b = run(n, seq)
print(" ".join(list(map(str, a))))
print(b)
```

