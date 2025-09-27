---
sidebar_position: 14
---

# Soal Array
kalo kurang ngerti boleh coba dlu sampe nyaman cara pake air
## Contol soal
### 1. Inisialisasi dan Cetak Array (Easy)

Buatlah program untuk menyimpan 5 nama buah dalam sebuah array string. Setelah itu, gunakan for loop untuk mencetak semua nama buah tersebut ke layar, masing-masing di baris baru.

Konsep: Deklarasi, inisialisasi, dan mengakses elemen array menggunakan loop.
**Contoh Output yang Diharapkan:**
```
Apel
Jeruk
Mangga
Anggur
Pisang
```
**Contoh Kode**
```c++
#include <iostream>
#include <string>
using namespace std;

int main() {
    string fruits[5] = {"Apel", "Jeruk", "Mangga", "Anggur", "Pisang"};
    
    for (int i = 0; i < 5; i++) {
        cout << fruits[i] << endl;
    }
    
    return 0;
}
```
### 2. Mencari Nilai Terbesar dalam Array (Easy)

Buatlah program yang memiliki sebuah array berisi bilangan bulat (misal: {10, 5, 30, 15, 25}). Program harus dapat menemukan dan mencetak nilai terbesar dari semua elemen dalam array tersebut.

Konsep: Iterasi array dan membandingkan elemen untuk mencari nilai maksimum.
**Contoh Output yang Diharapkan:**
```
Nilai terbesar dalam array adalah: 30
```

**Contoh Kode**
```c++
#include <iostream>
using namespace std;

int main() {
    int numbers[5] = {10, 5, 30, 15, 25};
    int max = numbers[0];
    
    for (int i = 1; i < 5; i++) {
        if (numbers[i] > max) {
            max = numbers[i];
        }
    }
    
    cout << "Nilai terbesar dalam array adalah: " << max << endl;
    
    return 0;
}
```

### Soal 3. Menghitung Rata-rata Nilai (Medium)

Buatlah program yang meminta pengguna untuk memasukkan 5 nilai ujian ke dalam sebuah array double. Setelah semua nilai dimasukkan, program harus menghitung dan menampilkan nilai rata-rata dari kelima ujian tersebut.

Konsep: Mengisi array dengan input pengguna, menjumlahkan semua elemen (sum), lalu membaginya dengan jumlah elemen.
**Contoh Interaksi:**
```
Masukkan nilai ujian ke-1: 80
Masukkan nilai ujian ke-2: 90
Masukkan nilai ujian ke-3: 75
Masukkan nilai ujian ke-4: 85
Masukkan nilai ujian ke-5: 95
Nilai rata-rata ujian adalah: 85
```
**Contoh Kode**
```c++
#include <iostream>
using namespace std;

int main() {
    double grades[5];
    double sum = 0;
    
    for (int i = 0; i < 5; i++) {
        cout << "Masukkan nilai ujian ke-" << i + 1 << ": ";
        cin >> grades[i];
        sum += grades[i];
    }
    
    double average = sum / 5;
    cout << "Nilai rata-rata ujian adalah: " << average << endl;
    
    return 0;
}
```
### 4. Membalik Urutan Elemen Array (Medium)

Buatlah sebuah program dengan array yang sudah diinisialisasi (misal: {1, 2, 3, 4, 5}). Program harus membalik urutan elemen di dalam array tersebut tanpa membuat array baru, lalu mencetak hasilnya.

Konsep: Menggunakan loop dan variabel sementara (temporary variable) untuk menukar elemen dari kedua ujung array (elemen pertama dengan terakhir, kedua dengan kedua terakhir, dst.).
**Contoh Output yang Diharapkan:**
```
Array setelah dibalik: 5 4 3 2 1
```
**Contoh Kode**
```c++
#include <iostream>
using namespace std;

int main() {
    int numbers[5] = {1, 2, 3, 4, 5};
    
    // Membalik urutan elemen array
    for (int i = 0; i < 5 / 2; i++) {
        // buat nampung nilai sementara `temp`
        int temp = numbers[i];
        numbers[i] = numbers[4 - i];
        numbers[4 - i] = temp;
    }
    
    // Mencetak array setelah dibalik
    cout << "Array setelah dibalik: ";
    for (int i = 0; i < 5; i++) {
        cout << numbers[i] << " ";
    }
    cout << endl;
    
    return 0;
}
```

### 5. Pencarian Data Siswa (Hard)

Buatlah dua buah array:

    string namaSiswa[4] = {"Budi", "Ani", "Citra", "Doni"};

    int nilaiSiswa[4] = {85, 92, 78, 88};

Program akan meminta pengguna memasukkan sebuah nama. Jika nama tersebut ada di dalam array namaSiswa, program akan mencetak nilai siswa yang bersangkutan. Jika tidak ada, cetak "Data tidak ditemukan".

Konsep: Menggunakan dua array paralel, mencari indeks dari elemen di array pertama, lalu menggunakan indeks yang sama untuk mengakses elemen di array kedua.
**Contoh Interaksi:**
```
Masukkan nama siswa yang dicari: Citra
Nilai Citra adalah: 78
```
**Contoh Kode**
```
#include <iostream>
#include <string>
using namespace std;

int main() {
    string namaSiswa[4] = {"Budi", "Ani", "Citra", "Doni"};
    int nilaiSiswa[4] = {85, 92, 78, 88};
    string namaDicari;
    bool ditemukan = false;
    
    cout << "Masukkan nama siswa yang dicari: ";
    getline(cin, namaDicari);
    
    for (int i = 0; i < 4; i++) {
        if (namaSiswa[i] == namaDicari) {
            cout << "Nilai " << namaDicari << " adalah: " << nilaiSiswa[i] << endl;
            ditemukan = true;
            break;
        }
    }
    
    if (!ditemukan) {
        cout << "Data tidak ditemukan" << endl;
    }
    
    return 0;
}
```

## Soal
### 1. Deklarasi dan Cetak Nilai Ujian (Easy)

Buatlah program untuk menyimpan 5 nilai ujian (misal: 85.5, 92.0, 78.5, 88.0, 95.5) dalam sebuah array float. Kemudian, gunakan for loop untuk mencetak semua nilai tersebut, lengkap dengan label "Nilai ke-x: ".

Konsep: Deklarasi, inisialisasi, dan iterasi array bertipe fContoh Output yang Diharapkan:
```
Nilai ke-1: 85.5
Nilai ke-2: 92
Nilai ke-3: 78.5
Nilai ke-4: 88
Nilai ke-5: 95.5
```

### 2. Mencari Nilai Terkecil dalam Array (Easy)

Buatlah program yang memiliki sebuah array berisi bilangan bulat (misal: {45, 67, 23, 12, 58}). Program harus dapat menemukan dan mencetak nilai terkecil dari semua elemen dalam array tersebut.

Konsep: Iterasi array dan membandingkan elemen untuk mencari nilai minimum.
Contoh Output yang Diharapkan:

Nilai terkecil dalam array adalah: 12

### 3. Menghitung Jumlah Bilangan Genap (Medium)

Buatlah program yang meminta pengguna untuk memasukkan 6 bilangan bulat ke dalam sebuah array. Setelah itu, program harus menghitung ada berapa banyak bilangan genap di dalam array tersebut dan menampilkannya.

Konsep: Mengisi array dengan input pengguna dan menggunakan operator modulo (%) di dalam loop untuk mengecek kondisi.
Contoh Interaksi:

Masukkan bilangan ke-1: 5
Masukkan bilangan ke-2: 8
Masukkan bilangan ke-3: 12
Masukkan bilangan ke-4: 3
Masukkan bilangan ke-5: 10
Masukkan bilangan ke-6: 7
Jumlah bilangan genap dalam array: 3

#### 4. Menggeser Elemen Array ke Kiri (Medium)

Buatlah program dengan array yang sudah diinisialisasi (misal: {1, 2, 3, 4, 5}). Program harus menggeser semua elemen array satu posisi ke kiri. Elemen pertama akan pindah menjadi elemen terakhir. Cetak hasilnya.

Konsep: Menyimpan elemen pertama dalam variabel sementara, lalu menggeser sisa elemen menggunakan loop, dan menempatkan elemen pertama di posisi terakhir.
Contoh Output yang Diharapkan:

Array setelah digeser ke kiri: 2 3 4 5 1

### 5. Filter Data Berdasarkan Kriteria (Hard)

Diberikan dua array paralel:
```
string produk[5] = {"Buku", "Pensil", "Tas", "Sepatu", "Meja"};
int harga[5] = {50000, 5000, 150000, 250000, 500000};
```
Buatlah program yang meminta pengguna memasukkan batas harga maksimal. Program kemudian akan menampilkan semua produk yang harganya di bawah atau sama dengan batas tersebut.
Konsep: Iterasi melalui array, menggunakan if untuk memfilter data berdasarkan input, dan menampilkan elemen yang sesuai dari array pertama.
Contoh Interaksi: