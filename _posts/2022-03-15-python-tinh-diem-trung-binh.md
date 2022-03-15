---
date:  2022-03-14 12:26:40
layout: post
title: Python - Tính điểm trung bình
subtitle: Tính điểm trung bình 3 môn Toán, Lý, Hoá bằng Python
description: Viết chương trình nhập vào điểm ba môn Toán, Lý, Hóa của một học sinh. In ra điểm trung bình của học sinh đó với hai số lẻ thập phân.
image: 
optimized_image: 
category: python
tags:
  - python
  - điểm
author: sloth
---

## Python - Tính điểm trung bình

Yêu cầu:

- Viết chương trình nhập vào điểm ba môn Toán, Lý, Hóa của một học sinh.
- In ra điểm trung bình của học sinh đó với hai số lẻ thập phân

Hướng dẫn: 

```python
toan = float(input("Nhập điểm Toán:"))
ly = float(input("Nhập điểm lý:"))
hoa = float(input("Nhập điểm hóa:"))
dtb = (toan+ly+hoa)/3
print("Điểm trung bình=",round(dtb,2))
```

