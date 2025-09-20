---
sidebar_position: 4
---

# CIN (Console Input)

`cin` adalah standard input dalam C++ yang digunakan untuk menerima input dari pengguna melalui console atau terminal. `cin` merupakan bagian dari library iostream.

## Sintaks Dasar

```cpp
cin >> variable;
```

## Contoh Penggunaan

```cpp
#include <iostream>
using namespace std;

int main() {
    // Input untuk tipe data string
    string nama;
    cout << "Masukkan nama: ";
    cin >> nama;

    // Input untuk tipe data integer
    int umur;
    cout << "Masukkan umur: ";
    cin >> umur;

    // Input beberapa nilai sekaligus
    int nilai1, nilai2;
    cout << "Masukkan dua angka: ";
    cin >> nilai1 >> nilai2;

    // Menampilkan hasil input
    cout << "Nama: " << nama << endl;
    cout << "Umur: " << umur << endl;
    cout << "Nilai 1: " << nilai1 << ", Nilai 2: " << nilai2 << endl;

    return 0;
}
```

## Tipe Data yang Didukung

1. **Integer (Bilangan Bulat)**
   ```cpp
   int angka;
   cin >> angka;
   ```

2. **Float/Double (Bilangan Desimal)**
   ```cpp
   float nilai;
   cin >> nilai;
   ```

3. **Character (Karakter)**
   ```cpp
   char huruf;
   cin >> huruf;
   ```

4. **String (Teks)**
   ```cpp
   string teks;
   cin >> teks;
   ```

## Catatan Penting

- Selalu sertakan library `<iostream>`
- `cin` hanya membaca sampai spasi atau enter

- Merupakan bagian dari `std` namespace

## Tips Tambahan

1. **Membaca String dengan Spasi**
   ```cpp
   string kalimat;
   getline(cin, kalimat);
   ```

## Input Multiple Value

`cin` dapat digunakan untuk menerima beberapa nilai sekaligus dalam satu baris dengan memisahkan nilai menggunakan spasi.

### Contoh Multiple Value

```cpp
#include <iostream>
using namespace std;

int main() {
    // Input multiple integer
    int a, b, c;
    cout << "Masukkan tiga angka: ";
    cin >> a >> b >> c;
    cout << "Nilai yang dimasukkan: " << a << " " << b << " " << c << endl;

    // Input multiple tipe data berbeda
    int umur;
    string nama;
    float tinggi;
    cout << "Masukkan umur nama tinggi: ";
    cin >> umur >> nama >> tinggi;
    cout << "Data: " << umur << " tahun, " << nama << ", " << tinggi << "cm" << endl;

    return 0;
}
```

### Tips Multiple Input
- Pisahkan setiap nilai dengan spasi saat input
- Pastikan urutan tipe data sesuai dengan variabel
- Dapat digunakan untuk tipe data yang berbeda
- Jumlah input harus sesuai dengan jumlah variabel
