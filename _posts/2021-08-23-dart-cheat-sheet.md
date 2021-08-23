---
layout: post
title: Dart Cheat Sheet
subtitle: Tài liệu ngắn gọn về ngôn ngữ lập trình Dart
categories: dart flutter
tags: [cheat sheet, dart, flutter]
---
Bạn có thể sử dụng các IDE như Android Studio, Visual Studio Code hoặc SublimeText để chạy thử các chương trình dưới đây. Hoặc đơn giản nhất là truy cập [dartpad](http://dartpad.dev/) để chạy thử chương trình ngay trên trình duyệt web mà không cần cài đặt.

## Một số quy ước chung

- Một câu lệnh `Dart` kết thúc bởi dấu chấm phảy `;`
- Một khối lệnh được đặt trong cặp ngoặc móc `{}`
- Chú thích trên một dòng được viết sau kí tự `//`, chú thích trên nhiều dòng nằm giữa cặp ký hiệu `/*` và `*/`

### Cách đặt tên biến, tên hàm, tên lớp

Một chương trình sử dụng rất nhiều *tên* hay còn gọi là *định danh* để làm tên chương trình, tên hàm, tên biến, tên hằng số…

- Tên trong Dart có độ dài tuỳ ý. Chúng có thể gồm cả chữ cái cả in hoa và in thường, các chữ số và dấu gạch dưới, nhưng bắt buộc phải bắt đầu bằng một chữ cái hoặc dấu gạch dưới. 
- Chúng ta nên đặt tên sao cho có ý nghĩa và dễ đọc (ngăn cách bởi dấu `_` hoặc viết hoa đầu mỗi từ...)

- Ký tự bắt đầu của tên phải là một dấu gạch dưới `_` hoặc một chữ cái (có thể là chữ hoa hoặc chữ thường). Tiếp theo có thể là một hoặc nhiều ký tự, con số hoặc thậm chí bỏ trống (tức tên chỉ gồm một kí tự).
- Trong tên không được có dấu cách trắng hoặc các ký tự đặc biệt như: `@ , $ . % ^ ! = + - * / % & ~\` 
- Tên không được trùng với các *từ khóa* của Dart.
- Tên của lớp, enum, tham số thường được đặt tên theo kiểu `UpperCamelCase`, tức là bắt đầu bởi chữ cái in hoa, ví dụ `MyClass`
- Tên biến, hằng, object, hàm thường đặt theokiểu `lowerCamelCase`, tức là bắt đầu bằng chữ cái thường và viết hoa đầu mỗi từ tiếp theo, ví dụ `myVar` hoặc `tinhGiaiThua`
- Viết tắt khi tên trên 2 từ, lấy ký đầu viết HOA để tạo chữ viết tắt, ví dụ `IOStream`  hoặc `InputOutputStream`
- Tên bắt đầu với một ký tự gạch dưới `_`  được hiểu rằng đây là một định danh *private* (riêng tư)

## Hàm `main`

Dart cũng giống như Java, mỗi chương trình Dart bắt đầu với một hàm `main`.  

```dart
main(){
    print('Hello World');
}
```

hoặc có thể viết gọn lại sử dụng `arrow function`

```dart
main() => print('Hello World');
```
Các đoạn mã dưới đây, mặc định đều được đặt trong một hàm `main()`

## Biến và các kiểu dữ liệu

### Biến là gì?

 để lưu các đối tượng khi ứng dụng hoạt động

### Khởi tạo biến

Để khởi tạo một biến, chúng ta sử dụng từ khoá `var` và theo sau là tên biến

```dart
var name;
var age;
```

Hoặc thay từ khoá `var` bằng kiểu dữ liệu của biến và theo sau là tên biến

```dart
String name;
int age;
```

### Phép gán

Để gán giá trị cho một biến, chúng ta sử dụng phép toán (toán tử - operator) `=`

```dart
name = 'Phương';
age = 31;
```

Chúng ta cũng có thể vừa khởi tạo một biến vừa gán cho nó một giá trị

```dart
String name = 'Phương';
int age = 31;
```

### Các kiểu dữ liệu mặc định `built-in types` của Dart

#### Static Types  

| Kiểu dữ liệu         | Mô tả                                                        |
| -------------------- | ------------------------------------------------------------ |
| `int `               | Dùng biểu diễn các số nguyên như `1` hoặc `-98`              |
| `double`             | Biểu diễn các số thực như `3.14`                             |
| `bool`               | Kiểu logic (Boolean) chỉ có hai giá trị `true` và `false`    |
| `String`             | Kiểu xâu (chuỗi) kí tự, Immutable string.                    |
| `StringBuffer`       | Mutable string.                                              |
| `RegExp`             | Kiểu biểu thức chính quy (Regular expressions)               |
| `List`, `Map`, `Set` | Các kiểu dữ liệu tập hợp: Danh sách (mảng, array), từ điển và tập hợp |
| `DateTime`           | A point in time.                                             |
| `Duration`           | A span of time.                                              |
| `Uri`                | Uniform Resource Identifier                                  |
| `Error`              | Error information                                            |

#### Dynamic Types

- The `var` keyword declares a variable without specifying its type, leaving the variable as a dynamic.
- The `dynamic` keyword declares a variable of the type `dynamic` with optional typing.  Khi biến có chấp nhận mọi kiểu thì sử dụng từ khóa `dynamic`

### Hằng số `const`

Để biểu diễn một hằng số trong Dart, chúng ta sử dụng từ khoá `const` và theo sau là tên của hằng số đó, ví dụ

```dart
const pi = 3.1415;
const 
```

Các hằng số là những giá trị cố định không thay đổi trong toàn bộ chương trình từ khi soạn thảo và khi chương trình chạy.

### Biến `final`

Trong chương trình, có những biến chỉ được nhận giá trị một lần và không bao giờ thay đổi (chẳng hạn địa chỉ email của một người) thì chúng ta sử dụng từ khoá `final` thay cho `var`



