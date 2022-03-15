---
date:  2022-03-15 12:26:40
layout: post
title: Python - Kiểm tra năm nhuận
subtitle: Kiểm tra xem một năm nhập vào có là năm nhuận không bằng Python
description: Nhập vào một năm bất kỳ, kiểm tra năm đó có phải năm nhuận hay không. Biết rằng Năm nhuận là năm chia hết cho 4 nhưng không chia hết cho 100 hoặc chia hết cho 400.
image: https://dummyfresher.com/assets/img/uploads/Leap-Day-and-Leap-Year.jpg
optimized_image: 
category: python
tags:
  - python
  - nhuận
author: sloth
---

## Python - Tính điểm trung bình

Yêu cầu: Nhập vào một năm bất kỳ, kiểm tra năm đó có phải năm nhuận hay không. 

<img src="https://dummyfresher.com/assets/img/uploads/Leap-Day-and-Leap-Year.jpg" alt="Leap-Day-and-Leap-Year" style="zoom:50%;" />

Hướng dẫn: 

{% youtube i-8Q3LksZjg %}

- Năm nhuận là năm chia hết cho 4 nhưng không chia hết cho 100 hoặc chia hết cho 400.
- Sử dụng câu lệnh điều kiện `if else`

```python
year=int(input("Mời Thím nhập vào 1 năm:"))
if (year % 4 ==0 and year % 100 != 0) or year % 400 == 0:
    print("Năm ", year, " là năm nhuận")
else:
    print("Năm ", year, " không nhuận")
```

