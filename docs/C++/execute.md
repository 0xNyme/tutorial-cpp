---
sidebar_position: 2
---

# Cara Mengeksekusi Program C++

Berikut adalah panduan langkah demi langkah untuk mengeksekusi program C++.

## Menggunakan Visual Studio Code

1. **Persiapan Awal**
   - Install Visual Studio Code
   - Install ekstensi C/C++ dari Microsoft
   - Install MinGW (compiler untuk C++)

2. **Membuat File C++**
   ```cpp
   // Buat file dengan ekstensi .cpp
   // Contoh: program.cpp
   #include <iostream>
   using namespace std;

   int main() {
       cout << "Hello World!";
       return 0;
   }
   ```

3. **Cara Kompilasi dan Eksekusi**
   - Buka terminal di VS Code
   - Kompilasi program:
     ```bash
     g++ program.cpp -o program
     ```
   - Jalankan program:
     ```bash
     ./program
     ```

## Menggunakan Command Prompt

1. **Kompilasi Program**
   ```bash
   g++ namafile.cpp -o output
   ```

2. **Jalankan Program**
   ```bash
   ./output
   ```

## Troubleshooting Umum

- Pastikan MinGW sudah terpasang dan ditambahkan ke PATH
- Periksa syntax error jika kompilasi gagal
- Pastikan berada di folder yang benar saat mengeksekusi

## Catatan Penting

- Selalu simpan file sebelum kompilasi
- Perhatikan pesan error saat kompilasi
- Gunakan ekstensi `.cpp` untuk file C++
- Program harus memiliki fungsi `main()`