---
date:  2022-03-14 12:26:40
layout: post
title: Python - Đổi số giây sang giờ phút giây
subtitle: Nhập vào số giây và đổi sang giờ phút giây bằng Python
description: Nhập vào số giây và đổi sang giờ phút giây bằng Python
image: 
optimized_image: 
category: python
tags:
  - python
  - thời gian 
author: sloth
---

## Python - Đổi số giây sang giờ phút giây

Yêu cầu:

- Nhập vào số giây bất kỳ `t` là một số nguyên. Tính và xuất ra dạng `HH:MM:SS`. 

- Ví dụ: Nhập vào `3750` thì xuất ra `1:2:30 AM`. Nhập `51100` thì xuất ra `2:11:40 PM`

Hướng dẫn: 

- Sử dụng phép toán chia lấy phần nguyên `%`
- Công thức cụ thể `hour=(t/3600)%24 `, `minute=(t%3600)/60`, `second=(t%3600)%60` 

Mã nguồn chương trình

```python
t=int(input("Nhập số giây:"))

hour=(t//3600)%24
minute=(t%3600)//60
second=(t%3600)%60

print(hour,":",minute,":",second)
```

