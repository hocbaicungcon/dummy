---
layout: post
title: Cách hiển thị công thức Toán trên website
subtitle: Hướng dẫn cách thêm thư viện MathJax để hiển thị công thức Toán LaTEX trên các website
categories: html
tags: [htmp, mathjax, wordpress]
---

## 1. Cách hiển thị công thức Toán trên website bất kì

Để hiển thị công thức toán trên website, chúng ta sẽ sử dụng thư viện **MathJax**. Bạn chỉ việc thêm đoạn mã sau vào phần giữa cặp thẻ `<head>` và `</head>`

```html
<script type="text/javascript" src="https://cdn.mathjax.org/mathjax/latest/MathJax.js">
MathJax.Hub.Config({
extensions: ["tex2jax.js","TeX/AMSmath.js","TeX/AMSsymbols.js"],
jax: ["input/TeX", "output/HTML-CSS"],
tex2jax: {
inlineMath: [ ['$','$'], ["\\(","\\)"] ],
displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
},
});
</script>
```

Khi đó, muốn hiển thị công thức toán, bạn sử dụng cách gõ LaTEX và đặt công thức muốn hiển thị 

- công thức trên cùng dòng văn bản trong cặp dấu `$`, hoặc `\(` và `\)` ví dụ

```html
Cho phương trình bậc hai $ax^2 + bx + c = 0$ hoặc \(ax^2 + bx + c = 0\)
```

Kết quả sẽ như thế này:

Cho phương trình bậc hai $ax^2 + bx + c = 0$

- công thức nằm riêng trên một dòng trong cặp dấu `$$`, hoặc `\[` và `\]` ví dụ

```html
Cho phương trình bậc hai $$ax^2 + bx + c = 0$$ hoặc \[ax^2 + bx + c = 0\]
```

Cho phương trình bậc hai
$$
ax^2 + bx + c = 0
$$

## 2. Cách hiển thị công thức Toán trên website Wordpress

Nguyên tắc vẫn là làm như trên, nhưng nhiều bạn không truy cập được vào hosting thì ta làm như sau:

Bạn đăng nhập Wordpress bằng tài khoản quản trị, chọn Appearance (Giao diện) rồi chọn tiếp Theme Editor (Sửa giao diện)

<img src="https://divin.dev/assets/images/image-20210826105952558.png" alt="image-20210826105952558" style="zoom:67%;" />

Bên góc trên tay phải, bạn chọn đúng theme muốn sửa rồi chọn tệp `header.php`

<img src="https://divin.dev/assets/images/image-20210826110210672.png" alt="image-20210826110210672" style="zoom:67%;" />

Trong tệp `header.php` bạn tìm đến cặp thẻ  `<head>` và `</head>` rồi làm tiếp như phần 1.

Cuối cùng, chọn Update File để lưu lại các thay đổi.

<img src="https://divin.dev/assets/images/image-20210826110505946.png" alt="image-20210826110505946" style="zoom:67%;" />
