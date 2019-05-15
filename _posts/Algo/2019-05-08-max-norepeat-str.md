---
layout: post
title: "无重复字符的最长子串"
subtitle: "The longest substring without duplicate characters"
author: "Aili"
header-style: text
catalog: true
tags:
  - 算法
  - 函数
---

## 题目：无重复字符的最长子串

> 给定一个字符串，请你找出其中不含有重复字符的 最长子串 的长度。

> 示例 1:
> 输入: "abcabcbb"
> 输出: 3 
> 解释: 因为无重复字符的最长子串是 "abc"，所以其长度为 3。

> 示例 2:
> 输入: "bbbbb"
> 输出: 1
> 解释: 因为无重复字符的最长子串是 "b"，所以其长度为 1。

> 示例 3:
> 输入: "pwwkew"
> 输出: 3

> 解释: 因为无重复字符的最长子串是 "wke"，所以其长度为 3。
>     请注意，你的答案必须是 子串 的长度，"pwke" 是一个子序列，不是子串。
     

#### 方法1:暴力查询

逐个检查所有的子字符串，看它是否不含有重复的字符。
 
``` java
/* 1.遍历出所有的子串
 *  2.检查每一个遍历出的子串是不是不重复。
 */
import java.util.HashSet;
import java.util.Set;
public class test1 {

    public static int lengthOfLongestSubstring(String s)
    {
        int n = s.length();
        int strmax=0;
        for (int i=0;i<n;i++)
        {
            for (int j=i+1;j<=n;j++)
            {
                strmax=(ifrepeat(s,i,j)>strmax)?ifrepeat(s,i,j):strmax;
            }
        }
        return strmax;
    }

    public static int ifrepeat(String s,int i,int j)
    {
        Set<Character> str = new HashSet<Character>();
        int strlen=0;
        for (int k=i;k<j;k++)
        {
            if (str.contains(s.charAt(k))==false)
            {
                str.add(s.charAt(k));
                strlen=str.size();
            }
            else
            {
                str.clear();
                continue;
            }

        }
        return strlen;
    }

    public static void main(String args[])
    {
          System.out.println(lengthOfLongestSubstring("pwwkew"));
    }
}
```

结果：
> 时间复杂度 O(n^3)

#### 方法1:滑动窗口

```java
import java.util.*;
public class Max_noreapt_str {
    public static int lengthOfLongestSubstring(String s) {
        int n = s.length();
        int strmax = 0;                          //最大子串的长度
        Map<Character, Integer> charstr = new HashMap();
        Character[] str = new Character[n];      // 最大子串的数组存放
        String maxstr = null;
        for (int i = 0, j = 0; j < n; j++) {
            if (charstr.containsKey(s.charAt(j))) {
                i = Math.max(charstr.get(s.charAt(j))+1, i);     //移动i的指针位置：当发现重复时，i的指针直接跳转到重复值的下一位，跳过已经判断过的子串
            }

            charstr.put(s.charAt(j), j);                       //插入字符和位置+重复时重写原有key值的value值，即更新该字符最新出现的位置。

            //未重复前的子串一定是当前不重复子串的最大串
            if (j - i + 1 > strmax) {
                strmax = j - i + 1;
                Iterator<Character> iter = charstr.keySet().iterator();
                while (iter.hasNext()) {
                    Character key = iter.next();
                    int value = Integer.parseInt(charstr.get(key).toString());
                    str[value] = key;
                }
                maxstr = Arrays.toString(Arrays.copyOfRange(str, i, (j + 1)));  // Arrays.copyOfRange(oldArray, startIndex, endIndex);startIndex是要复制的范围的初始索引（包括）,endIndex是要复制的范围的最终索引，不包括。 （此索引可能位于数组之外）
            }
        }
        charstr.clear();

        System.out.println(maxstr);
        return strmax;
    }

    public static void main(String args[]) {
        System.out.println(lengthOfLongestSubstring("wpwkewab"));
    }
}

```
结果：

```
[k, e, w, a, b]
5
```
