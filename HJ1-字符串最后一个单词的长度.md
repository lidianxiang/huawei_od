## 1. 题目描述

计算字符串最后一个单词的长度，单词以空格隔开，字符串长度小于5000。（注：字符串末尾不以空格为结尾）

示例：

```
输入：hello nowcoder
输出：8
说明：最后一个单词为nowcoder，长度为8   
```



## Solution

```python
import sys

str = input()
arr = str.split(" ")
print(len(arr[-1]))
```

