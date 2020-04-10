---
layout: post
title:  "Unix Timestamp From date Command in Mac OSX"
date:   2020-04-09 14:42:28 PST
categories: utils
---

## Date from Unix Timestamp

```shell
[14:23 ~    ] % date -r 1586467412
Thu Apr  9 14:23:32 PDT 2020
```

## Unix Timestamp by relative date
We can get unix timestamp for a relative day. Below example shows how to get unix timestamp for a one day in the past from current time.

```shell
[14:23 ~    ] % date -v -1d +%s
1586467412
```


