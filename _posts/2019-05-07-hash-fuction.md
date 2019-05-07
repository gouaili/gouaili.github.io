---
layout: post
title: "散列/哈希函数"
subtitle: "散列/哈希函数"
author: "Aili"
header-mask: 0.2
catalog: true
tags:
  - 函数
  - 密码
---

## 什么是哈希 

散列（英语：Hashing）是计算机科学中一种对数据的处理方法，通过某种特定的函数/算法（称为散列函数/算法）将要检索的项与用来检索的索引（称为散列，或者散列值）关联起来，生成一种便于搜索的数据结构（称为散列表）。

> 哈希函数就是一种映射，是从关键字到存储地址的映射。


## 应用 

* 密码学： MD5，SHA-256
* 数据结构： 


## 当前哈希函数  


下面是当前：

| 算法名称	| 输出大小（bits）|内部大小|区块大小	|长度大小|字符尺寸|碰撞情形|
| :----: |:----: |:----: |:----: |:----: |:----: |:----: |
|HAVAL|256/224/192/160/128	|256	|1024	|64	|32|	是|
|MD2|	128	|384	|128|	No	|8	|大多数|
|MD4|128|	128	|512|	64	|32|	是|
|MD5|128	|128|	512	|64 |32|	是|
|PANAMA|256	|8736|256|	否	|32|	是|
|RadioGatún|Arbitrarily long|58 words|3 words|否|	1-64|	否|
|RIPEMD|	128	|128|	512	|64	|32	|是|
RIPEMD-128/256|	128/256	|128/256	|512	|64|	32|	否|
|RIPEMD-160/320	|160/320	|160/320|	512	|64	|32	|否|
|SHA-0|160|	160	|512|	64|	32|	是|
|SHA-1|	160|	160	|512	|64	|32	|有缺陷|
|SHA-256/224|	256/224	|256|	512	|64|	32|	否|
|SHA-512/384	|512/384|	512|	1024|	128	|64|	否|
|Tiger（2）-192/160/128	|192/160/128|	192	|512|	64|	64|	否|
|WHIRLPOOL	|512	|512|	512|	256|	8	|否|

<html xmlns:o="urn:schemas-microsoft-com:office:office"
xmlns:x="urn:schemas-microsoft-com:office:excel"
xmlns="http://www.w3.org/TR/REC-html40">

<head>
<meta http-equiv=Content-Type content="text/html; charset=x-mac-chinesesimp">
<meta name=ProgId content=Excel.Sheet>
<meta name=Generator content="Microsoft Excel 15">
<link rel=File-List href="¹¤×÷²¾1.fld/filelist.xml">
<style>
<!--table
	{mso-displayed-decimal-separator:"\.";
	mso-displayed-thousand-separator:"\,";}
@page
	{margin:.75in .7in .75in .7in;
	mso-header-margin:.3in;
	mso-footer-margin:.3in;}
.style0
	{mso-number-format:General;
	text-align:general;
	vertical-align:bottom;
	white-space:nowrap;
	mso-rotate:0;
	mso-background-source:auto;
	mso-pattern:auto;
	color:black;
	font-size:12.0pt;
	font-weight:400;
	font-style:normal;
	text-decoration:none;
	font-family:DengXian;
	mso-generic-font-family:auto;
	mso-font-charset:134;
	border:none;
	mso-protection:locked visible;
	mso-style-name:³£¹æ;
	mso-style-id:0;}
td
	{mso-style-parent:style0;
	padding-top:1px;
	padding-right:1px;
	padding-left:1px;
	mso-ignore:padding;
	color:black;
	font-size:12.0pt;
	font-weight:400;
	font-style:normal;
	text-decoration:none;
	font-family:DengXian;
	mso-generic-font-family:auto;
	mso-font-charset:134;
	mso-number-format:General;
	text-align:general;
	vertical-align:bottom;
	border:none;
	mso-background-source:auto;
	mso-pattern:auto;
	mso-protection:locked visible;
	white-space:nowrap;
	mso-rotate:0;}
.xl65
	{mso-style-parent:style0;
	text-align:center;}
.xl66
	{mso-style-parent:style0;
	color:#404040;
	font-size:16.0pt;
	font-weight:700;
	font-family:Î¢ÈíÑÅºÚ;
	mso-generic-font-family:auto;
	mso-font-charset:134;
	text-align:center;
	border:.5pt solid windowtext;
	background:#D9D9D9;
	mso-pattern:black none;}
.xl67
	{mso-style-parent:style0;
	color:#404040;
	font-size:16.0pt;
	font-family:"Helvetica Neue";
	mso-generic-font-family:auto;
	mso-font-charset:0;
	text-align:center;
	border:.5pt solid windowtext;}
ruby
	{ruby-align:left;}
rt
	{color:windowtext;
	font-size:9.0pt;
	font-weight:400;
	font-style:normal;
	text-decoration:none;
	font-family:DengXian;
	mso-generic-font-family:auto;
	mso-font-charset:134;
	mso-char-type:none;
	display:none;}
-->
</style>
</head>

<body link="#0563C1" vlink="#954F72">
<meta charset=utf-8>

<table border=0 cellpadding=0 cellspacing=0 width=1034 style='border-collapse:
 collapse;table-layout:fixed;width:775pt;box-sizing: border-box;border-spacing: 0px;
 max-width: 100%;font-variant-ligatures: normal;font-variant-caps: normal;
 orphans: 2;text-align:start;widows: 2;-webkit-text-stroke-width: 0px;
 text-decoration-style: initial;text-decoration-color: initial'>
 <col class=xl65 width=271 style='mso-width-source:userset;mso-width-alt:8661;
 width:203pt'>
 <col class=xl65 width=265 style='mso-width-source:userset;mso-width-alt:8490;
 width:199pt'>
 <col class=xl65 width=116 style='mso-width-source:userset;mso-width-alt:3712;
 width:87pt'>
 <col class=xl65 width=121 style='mso-width-source:userset;mso-width-alt:3882;
 width:91pt'>
 <col class=xl65 width=87 span=3 style='width:65pt'>
 <tr height=31 style='height:23.0pt;box-sizing: border-box'>
  <td height=31 class=xl66 width=271 style='height:23.0pt;width:203pt'>Ëã·¨Ãû³Æ</td>
  <td class=xl66 width=265 style='border-left:none;width:199pt'>Êä³ö´óÐ¡£¨bits£©</td>
  <td class=xl66 width=116 style='border-left:none;width:87pt'>ÄÚ²¿´óÐ¡</td>
  <td class=xl66 width=121 style='border-left:none;width:91pt'>Çø¿é´óÐ¡</td>
  <td class=xl66 width=87 style='border-left:none;width:65pt'>³¤¶È´óÐ¡</td>
  <td class=xl66 width=87 style='border-left:none;width:65pt'>×Ö·û³ß´ç</td>
  <td class=xl66 width=87 style='border-left:none;width:65pt'>Åö×²ÇéÐÎ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>HAVAL</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>256/224/192/160/128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>256</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>1024</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>32</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>ÊÇ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>MD2</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>384</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>No</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>8</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>´ó¶àÊý</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>MD4</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>32</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>ÊÇ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>MD5</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>32</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>ÊÇ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>PANAMA</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>256</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>8736</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>256</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>·ñ</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>32</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>ÊÇ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>RadioGat¨²n</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>Arbitrarily
  long</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>58
  words</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>3
  words</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>·ñ</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>1-64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>·ñ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>RIPEMD</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>32</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>ÊÇ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>RIPEMD-128/256</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128/256</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128/256</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>32</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>·ñ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>RIPEMD-160/320</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>160/320</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>160/320</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>32</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>·ñ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>SHA-0</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>160</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>160</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>32</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>ÊÇ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>SHA-1</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>160</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>160</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>32</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>ÓÐÈ±ÏÝ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>SHA-256/224</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>256/224</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>256</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>32</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>·ñ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>SHA-512/384</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512/384</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>1024</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>·ñ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>Tiger£¨2£©-192/160/128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>192/160/128</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>192</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>64</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>·ñ</td>
 </tr>
 <tr height=27 style='height:20.0pt;box-sizing: border-box'>
  <td height=27 class=xl67 style='height:20.0pt;border-top:none;box-sizing: border-box'>WHIRLPOOL</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>512</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>256</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>8</td>
  <td class=xl67 style='border-top:none;border-left:none;box-sizing: border-box'>·ñ</td>
 </tr>
</table>

</body>

</html>



**"Welcome to the producer side!"**
