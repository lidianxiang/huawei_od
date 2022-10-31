## 1. 题目描述

一个 DNA 序列由 A/C/G/T 四个字母的排列组合组成。 G 和 C 的比例（定义为 GC-Ratio ）是序列中 G 和 C 两个字母的总的出现次数除以总的字母数目（也就是序列长度）。在基因工程中，这个比例非常重要。因为高的 GC-Ratio 可能是基因的起始点。

给定一个很长的 DNA 序列，以及限定的子串长度 N ，请帮助研究人员在给出的 DNA 序列中从左往右找出 GC-Ratio 最高且长度为 N 的第一个子串。

DNA序列为 ACGT 的子串有: ACG , CG , CGT 等等，但是没有 AGT ， CT 等等



示例1:

```
输入：
    ACGT
    2
输出：CG
说明：ACGT长度为2的子串有AC,CG,GT3个，其中AC和GT2个的GC-Ratio都为0.5，CG为1，故输出CG   
```



## 2. 思路

巧用count()函数：str.count(sub, start=0, end=len(string))

sub为搜索的子字符串，start为字符串开始搜索的位置，end为字符串中结束搜索的位置



## 3. Solution

```python
while True:
    try:
        DNA = input()
        length = int(input())
        max_counts = 0
        max_DNA = []
        for i in range(len(DNA) - length + 1):
            GC_counts = DNA.count('G', i, i+length) + DNA.count('C', i, i+length)
            if GC_counts > max_counts:
                max_counts = GC_counts
                max_DNA = DNA[i:i+length]
        print(max_DNA)
    except:
        break
```

