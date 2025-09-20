---
sidebar_position: 9
---

# Latihan Pemrograman C++

## 1. Kalkulator Sederhana

Program kalkulator yang dapat melakukan operasi dasar (+, -, *, /).

```cpp
#include <iostream>
using namespace std;

int main() {
    // kita buat variabel untuk menampung angka nya terlebih dahulu dan juga operasi nya
    float angka1, angka2;
    // buat variabel untuk menampung operasi nya
    char operasi;
    
    // Input angka dan operasi
    cout << "Masukkan angka pertama: ";
    cin >> angka1;
    cout << "Masukkan operasi (+,-,*,/): ";
    cin >> operasi;
    cout << "Masukkan angka kedua: ";
    cin >> angka2;
    
    // check apakah operasi sama dengan yang diminta menggunakan if statement misalkan operasi nya isinya "+" sama dengan "+"
    if (operasi == '+') {
        // maka lakukan operasi penjumlahan jika operasi sesuai begitu seterusnya
        cout << "Hasil: " << angka1 + angka2;
    } else if (operasi == '-') {
        cout << "Hasil: " << angka1 - angka2;
    } else if (operasi == '*') {
        cout << "Hasil: " << angka1 * angka2;
    } else if (operasi == '/') {
        // di bagian pembagian kita harus cek kalo angka gk boleh sama dengan nol agak tidak terjadi angka / 0 
        if (angka2 != 0) {
            cout << "Hasil: " << angka1 / angka2;
        } else {
            cout << "Error: Pembagian dengan nol!";
        }
    } else {
        cout << "Operasi tidak valid!";
    }
    
    return 0;
}
```


## 2. Cek Bilangan Prima

Program untuk mengecek apakah sebuah angka adalah bilangan prima.

```cpp
#include <iostream>
using namespace std;

int main() {
    int angka;
    bool isPrima = true;
    
    cout << "Masukkan angka: ";
    cin >> angka;
    
    // Cek apakah angka kurang dari 2
    if (angka < 2) {
        isPrima = false;
    } else {
        // Cek pembagian dari 2 sampai angka-1
        for (int i = 2; i < angka; i++) {
            if (angka % i == 0) {
                isPrima = false;
                break;
            }
        }
    }
    
    // Tampilkan hasil
    if (isPrima) {
        cout << angka << " adalah bilangan prima";
    } else {
        cout << angka << " bukan bilangan prima";
    }
    
    return 0;
}
```

**Penjelasan:**
1. Input sebuah angka
2. Cek jika angka kurang dari 2 (bukan prima)
3. Loop dari 2 sampai angka-1 untuk cek pembagian
4. Jika ada pembagian yang habis, maka bukan prima
5. Tampilkan hasil pengecekan

## 3. Pola Segitiga Angka

Program untuk membuat pola segitiga dengan angka.

```cpp
#include <iostream>
using namespace std;

int main() {
    int tinggi;
    
    cout << "Masukkan tinggi segitiga: ";
    cin >> tinggi;
    
    // Loop untuk setiap baris sebanyak tinggi nya
    for (int i = 1; i <= tinggi; i++) {
        // Loop untuk setiap kolom
        // cetak nilai j sebanyak i lalu bri spasi
        for (int j = 1; j <= i; j++) {
            cout << j << " ";
        }
        // cetak baris baru
        cout << endl;
    }
    
    return 0;
}
```

**Penjelasan:**
1. Input tinggi segitiga
2. Loop pertama untuk mengatur baris (i)
3. Loop kedua untuk mencetak angka dalam satu baris
4. Setiap baris mencetak angka dari 1 sampai nilai i
5. Tambah baris baru setelah setiap baris selesai

Output untuk tinggi = 5:
```
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5
```

## 4. Menghitung Rata-rata

Program untuk menghitung rata-rata dari sejumlah nilai.

```cpp
#include <iostream>
using namespace std;

int main() {
    int jumlah;
    float nilai, total = 0, rata;
    
    cout << "Masukkan jumlah nilai: ";
    cin >> jumlah;
    
    // Input nilai dan hitung total
    // loop i sebanyak nilai jumlah 
    for (int i = 1; i <= jumlah; i++) {
        // input nilai yang ingin di jumlahkan
        cout << "Masukkan nilai ke-" << i << ": ";
        cin >> nilai;
        // total = total + nilai
        // artinya nilai total berubah setiap looping dan akan terus di tambahkan sebanyak
        // jumlah
        total += nilai;
    }
    
    // Hitung dan tampilkan rata-rata
    rata = total / jumlah;
    cout << "Rata-rata: " << rata;
    
    return 0;
}
```

**Penjelasan:**
1. Input jumlah nilai yang akan dimasukkan
2. Loop sebanyak jumlah nilai untuk input
3. Setiap nilai ditambahkan ke variabel total
4. Hitung rata-rata dengan membagi total dengan jumlah
5. Tampilkan hasil rata-rata

## 5. Game Tebak Angka

Program sederhana untuk menebak angka antara 1-100.

```cpp
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    // Generate angka random
    srand(time(0));
    int angkaRahasia = rand() % 100 + 1;
    int tebakan;
    int percobaan = 0;
    
    cout << "=== Game Tebak Angka 1-100 ===" << endl;
    
    do {
        cout << "Masukkan tebakan: ";
        cin >> tebakan;
        percobaan++;
        
        if (tebakan < angkaRahasia) {
            cout << "Terlalu kecil!" << endl;
        } else if (tebakan > angkaRahasia) {
            cout << "Terlalu besar!" << endl;
        } else {
            cout << "Selamat! Anda benar setelah " << percobaan << " percobaan" << endl;
        }
    } while (tebakan != angkaRahasia);
    
    return 0;
}
```

**Penjelasan:**
1. Generate angka random 1-100
2. Gunakan do-while untuk terus meminta tebakan
3. Beri petunjuk "terlalu besar" atau "terlalu kecil"
4. Hitung jumlah percobaan yang dibutuhkan
5. Program selesai ketika tebakan benar

## 6. Konversi Suhu

Program untuk mengkonversi suhu antar satuan (Celsius, Fahrenheit, Kelvin).

```cpp
#include <iostream>
using namespace std;

int main() {
    float suhu;
    char dari, ke;
    float hasil;
    
    cout << "Masukkan suhu: ";
    cin >> suhu;
    cout << "Dari satuan (C/F/K): ";
    cin >> dari;
    cout << "Ke satuan (C/F/K): ";
    cin >> ke;
    
    // Konversi ke Celsius dulu
    float celsius;
    if (dari == 'C' || dari == 'c') {
        celsius = suhu;
    } else if (dari == 'F' || dari == 'f') {
        celsius = (suhu - 32) * 5/9;
    } else if (dari == 'K' || dari == 'k') {
        celsius = suhu - 273.15;
    }
    
    // Konversi dari Celsius ke tujuan
    if (ke == 'C' || ke == 'c') {
        hasil = celsius;
    } else if (ke == 'F' || ke == 'f') {
        hasil = (celsius * 9/5) + 32;
    } else if (ke == 'K' || ke == 'k') {
        hasil = celsius + 273.15;
    }
    
    cout << "Hasil konversi: " << hasil;
    
    return 0;
}
```

**Penjelasan:**
1. Input suhu dan satuan awal dan tujuan
2. Konversi input ke Celsius terlebih dahulu
3. Konversi dari Celsius ke satuan tujuan
4. Gunakan rumus konversi yang sesuai
5. Tampilkan hasil konversi



