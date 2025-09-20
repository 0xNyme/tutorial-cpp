---
sidebar_position: 6
---

# Operator dalam C++

Berikut adalah penjelasan tentang operator-operator yang umum digunakan dalam C++.

## 1. Operator Aritmatika

```cpp
int a = 10, b = 3;

cout << "Penjumlahan: " << a + b << endl;     // Output: 13
cout << "Pengurangan: " << a - b << endl;      // Output: 7
cout << "Perkalian: " << a * b << endl;       // Output: 30
cout << "Pembagian: " << a / b << endl;       // Output: 3
cout << "Sisa Bagi (Modulo): " << a % b << endl;  // Output: 1
```

## 2. Operator Perbandingan

```cpp
int x = 5, y = 10;

cout << "x == y: " << (x == y) << endl;  // Equal to (false)
cout << "x != y: " << (x != y) << endl;  // Not equal to (true)
cout << "x < y: " << (x < y) << endl;    // Less than (true)
cout << "x > y: " << (x > y) << endl;    // Greater than (false)
cout << "x <= y: " << (x <= y) << endl;  // Less than or equal (true)
cout << "x >= y: " << (x >= y) << endl;  // Greater than or equal (false)
```

## 3. Operator Logika

```cpp
bool p = true, q = false;

cout << "AND (&&): " << (p && q) << endl;  // false
cout << "OR (||): " << (p || q) << endl;   // true
cout << "NOT (!): " << (!p) << endl;       // false
```

## 4. Operator Assignment

```cpp
int nilai = 10;

nilai += 5;  // nilai = nilai + 5
cout << "+=: " << nilai << endl;  // 15

nilai -= 3;  // nilai = nilai - 3
cout << "-=: " << nilai << endl;  // 12

nilai *= 2;  // nilai = nilai * 2
cout << "*=: " << nilai << endl;  // 24

nilai /= 4;  // nilai = nilai / 4
cout << "/=: " << nilai << endl;  // 6

nilai %= 4;  // nilai = nilai % 4
cout << "%=: " << nilai << endl;  // 2
```

## 5. Operator Increment/Decrement

```cpp
int i = 5;

cout << "Pre-increment: " << ++i << endl;   // 6 (increment dulu, lalu print)
cout << "Post-increment: " << i++ << endl;  // 6 (print dulu, lalu increment)
cout << "Nilai sekarang: " << i << endl;    // 7

cout << "Pre-decrement: " << --i << endl;   // 6 (decrement dulu, lalu print)
cout << "Post-decrement: " << i-- << endl;  // 6 (print dulu, lalu decrement)
cout << "Nilai sekarang: " << i << endl;    // 5
```

## 6. Operator Bitwise

```cpp
int a = 5;  // 101 dalam biner
int b = 3;  // 011 dalam biner

cout << "AND (&): " << (a & b) << endl;   // 1 (001)
cout << "OR (|): " << (a | b) << endl;    // 7 (111)
cout << "XOR (^): " << (a ^ b) << endl;   // 6 (110)
cout << "Left shift (<<): " << (a << 1) << endl;   // 10 (1010)
cout << "Right shift (>>): " << (a >> 1) << endl;  // 2 (010)
```

## Contoh Program Lengkap

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10, b = 3;
    
    // Operasi aritmatika
    cout << "Aritmatika:" << endl;
    cout << a << " + " << b << " = " << (a + b) << endl;
    cout << a << " - " << b << " = " << (a - b) << endl;
    
    // Operasi perbandingan
    cout << "\nPerbandingan:" << endl;
    cout << a << " > " << b << " adalah " << (a > b) << endl;
    
    // Operasi logika
    bool p = true, q = false;
    cout << "\nLogika:" << endl;
    cout << "p AND q = " << (p && q) << endl;
    
    return 0;
}
```

## Catatan Penting

- Perhatikan urutan operasi (operator precedence)
- Gunakan tanda kurung untuk mengatur prioritas operasi
- Operator logika menghasilkan nilai boolean (true/false)
- Operator increment/decrement memiliki versi prefix dan postfix
- Operator bitwise bekerja pada level bit