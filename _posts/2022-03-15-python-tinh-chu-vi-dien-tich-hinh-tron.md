---
date:  2022-03-14 12:26:40
layout: post
title: Python - Tính chu vi và diện tích hình tròn
subtitle: Tính chu vi và diện tích hình tròn khi nhập bán kính bằng Python
description: Tính chu vi và diện tích hình tròn khi nhập bán kính bằng Python.
image: 
optimized_image: 
category: python
tags:
  - python
  - chu vi
  - diện tích
  - hình tròn
author: sloth
---

## Tính chu vi diện tích hình tròn

Yêu cầu:

Nhập bán kính đường tròn r. Tính và xuất chu vi, diện tích đường tròn tương ứng. 

Hướng dẫn: 

- Công thức tính chu vi đường tròn là $2\pi r$ và diện tích là $\pi r^2r$.
- Sử dụng thư viện `math` để lấy giá trị số $\pi$

Mã nguồn chương trình

```python
import math

try:
    r = float(input("Nhập bán kính hình tròn:"))   
    print("Chu vi =", 2*math.pi*r)
    print("Diện tích =", math.pi*r*r)
except:
    print("Bạn nhập bán kính bị lỗi!")
```
