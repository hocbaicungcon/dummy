---
layout: post
title: Đọc số tự nhiên
subtitle: 
categories: dart
tags: [dart, flutter]
---

# Bài tập Dart - Đọc số tự nhiên

Viết chương trình in ra cách đọc của một số tự nhiên `n` cho trước có ba chữ số. Ví dụ với `n=123` thì kết quả in ra màn hình là `Một trăm hai mươi ba`

Dưới đây, chúng tôi gợi ý bạn sử dụng từ khóa `switch case` để giải quyết. Nếu sử dụng kiểu dữ liệu `List` hoặc `Map` thì chương trình sẽ gọn hơn rất nhiều.

```dart
import 'dart:io';
import 'dart:math';

void main() {
  final random = Random();
  int n = random.nextInt(100);
  int so_lan_doan = 0;

  while (so_lan_doan < 3) {
    stdout.write('Mời bạn đoán một số:');
    int so_du_doan = int.parse(stdin.readLineSync()!);
    so_lan_doan++;
    if (so_du_doan == n) {
      print('Chúc mừng! Bạn đoán chính xác!');
      break;
    } else if (so_du_doan < n) {
      print('Số bạn đoán nhỏ hơn số của chương trình!');
    } else {
      print('Số bạn đoán lớn hơn số của chương trình!');
    }
  }
  if (so_lan_doan == 3) print('Bạn đã thua cuộc!');
}
```
