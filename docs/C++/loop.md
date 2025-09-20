---
sidebar_position: 8
---

# Loops (Perulangan) dalam C++

Perulangan memungkinkan kita untuk mengeksekusi blok kode secara berulang. Berikut adalah jenis-jenis perulangan dalam C++.

## 1. For Loop

For loop digunakan ketika kita tahu berapa kali kita ingin mengulang sesuatu.

```cpp
for (inisialisasi; kondisi; increment/decrement) {
    // kode yang diulang
}
```

Contoh:
```cpp
// Menampilkan angka 1-5
for (int i = 1; i <= 5; i++) {
    cout << i << " ";
}  // Output: 1 2 3 4 5
```

## 2. While Loop

While loop akan terus mengulang selama kondisi bernilai true.

```cpp
while (kondisi) {
    // kode yang diulang
}
```

Contoh:
```cpp
int i = 1;
while (i <= 5) {
    cout << i << " ";
    i++;
}  // Output: 1 2 3 4 5
```

## 3. Do-While Loop

Do-While loop mirip dengan while loop, tapi minimal akan dieksekusi satu kali.

```cpp
do {
    // kode yang diulang
} while (kondisi);
```

Contoh:
```cpp
int i = 1;
do {
    cout << i << " ";
    i++;
} while (i <= 5);  // Output: 1 2 3 4 5
```

## 4. Nested Loops (Perulangan Bersarang)

```cpp
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 3; j++) {
        cout << i << "," << j << " ";
    }
    cout << endl;
}
```

Output:
```
1,1 1,2 1,3
2,1 2,2 2,3
3,1 3,2 3,3
```

## 5. Loop Control Statements

### Break Statement
```cpp
for (int i = 1; i <= 5; i++) {
    // kita loop jika nilai i = dengan 3 pada if statement maka looping di hentikan
    if (i == 3) break;
    cout << i << " ";
}  // Output: 1 2
```

### Continue Statement
```cpp
for (int i = 1; i <= 5; i++) {
    // kita loop jika nilai i == 3 maka loop ini akan kita lewati atau gak ngapa ngapain
    if (i == 3) continue;
    cout << i << " ";
}  // Output: 1 2 4 5
```

## Contoh Program Lengkap

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Masukkan jumlah bintang: ";
    cin >> n;
    
    // Membuat pola segitiga
    // kita looping sebanyak n
    for (int i = 1; i <= n; i++) {
        // kita looping lagi mengikuti loop sebelumny menggunakan j lets say loop ke - 1 maka cuma keluar 1 bintang lalu baris baru
        // jika loop kedua maka akan keluar 2 bintang lalu baris baru
        // dan loop j akan direset dari 1 jika i sudah ganti angka
        for (int j = 1; j <= i; j++) {
            // 
            cout << "* ";
        }
        cout << endl;
    }
    
    return 0;
}
```

Output untuk n = 5:
```
* 
* * 
* * * 
* * * * 
* * * * *
```

## Catatan Penting

- Pilih jenis loop yang sesuai dengan kebutuhan:
  - `for`: ketika tahu jumlah iterasi
  - `while`: ketika tidak tahu jumlah iterasi
  - `do-while`: ketika perlu eksekusi minimal sekali
- Hindari infinite loop (loop tanpa akhir)
- Pastikan kondisi loop akan berakhir
- Gunakan `break` untuk keluar dari loop
- Gunakan `continue` untuk melompati iterasi
- Perhatikan increment/decrement counter