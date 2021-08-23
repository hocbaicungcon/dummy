---
layout: post
title: Dart Cheat Sheet
subtitle: Tài liệu ngắn gọn về ngôn ngữ lập trình Dart
categories: dart flutter
tags: [cheat sheet, dart, flutter]
---
## Entry Point

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
## Biến và các kiểu dữ liệu

### Biến là gì và cách đặt tên biến

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

### Các kiểu dữ liệu của Dart

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
- The `dynamic` keyword declares a variable of the type `dynamic` with optional typing.  

