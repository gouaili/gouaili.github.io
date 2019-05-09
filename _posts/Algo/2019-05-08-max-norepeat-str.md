---
layout: post
title: "The longest substring without duplicate characters"
subtitle: "no "
author: "Aili"
date:
tags:
  - Web
  - Wechat
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
        //System.out.println(n);
        int strmax=0;
        for (int i=0;i<=n;i++)
        {
            for (int j=i;j<=n;j++)
            {
                //System.out.println(s.substring(i,j));
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
                //System.out.println(str);
                strlen=str.size();
                //System.out.println(strlen);
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
