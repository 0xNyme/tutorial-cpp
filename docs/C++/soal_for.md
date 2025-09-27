---
sidebar_position: 13
---

# Soal Latihan Loop

## Contoh soal
### 1. Cetak Kalimat Sebanyak N Kali (Easy)

Buatlah program yang meminta pengguna memasukkan sebuah bilangan bulat N. Kemudian, program akan mencetak kalimat "Belajar C++ itu menyenangkan!" sebanyak N kali.

Konsep: Penggunaan for loop sederhana untuk iterasi sejumlah kali yang sudah ditentukan.

**Contoh Input:**
```
Masukkan jumlah perulangan: 5
```
**Contoh Output:**
```
Belajar C++ itu menyenangkan!
Belajar C++ itu menyenangkan!
Belajar C++ itu menyenangkan!
Belajar C++ itu menyenangkan!
Belajar C++ itu menyenangkan!
```
**Contoh Kode**
```cpp
#include <iostream>
using namespace std;

int main() {
    int N;
    cout << "Masukkan jumlah perulangan: ";
    cin >> N;
    
    for (int i = 0; i < N; i++) {
        cout << "Belajar C++ itu menyenangkan!" << endl;
    }
    
    return 0;
}
```

### 2. Menghitung Jumlah (Sum) Bilangan (Easy)

Buatlah program yang meminta pengguna memasukkan sebuah bilangan bulat positif N. Program akan menghitung dan menampilkan total penjumlahan dari semua bilangan dari 1 sampai N (1 + 2 + 3 + ... + N).

Konsep: Menggunakan for loop dengan variabel accumulator (penampung) untuk menjumlahkan nilai pada setiap iterasi.
**Contoh Input:**
```
Masukkan bilangan N: 10
```
**Contoh Output:**
```
Jumlah dari 1 sampai 10 adalah: 55
```
**Contoh Kode**
```cpp
#include <iostream>
using namespace std;

int main() {
    int N, sum = 0;
    cout << "Masukkan bilangan N: ";
    cin >> N;
    
    for (int i = 1; i <= N; i++) {
        sum += i;
    }
    
    cout << "Jumlah dari 1 sampai " << N << " adalah: " << sum << endl;
    
    return 0;
}
```

### 3. Game Tebak Angka (Medium)

Buatlah sebuah game tebak angka sederhana. Tentukan sebuah angka_rahasia di dalam kode (misal: 78). Program akan terus meminta pengguna menebak angka sampai tebakannya benar.

- Jika tebakan pengguna lebih kecil dari angka_rahasia, cetak "Terlalu rendah".

- Jika tebakan lebih besar, cetak "Terlalu tinggi".

- Jika tebakan benar, cetak "Selamat, tebakan Anda benar!" dan hentikan perulangan.

Konsep: Penggunaan while loop yang kondisinya bergantung pada input pengguna, dikombinasikan dengan if-else di dalamnya.

**Contoh Interaksi:**
```
Tebak angka (1-100): 50
Terlalu rendah
Tebak angka (1-100): 80
Terlalu tinggi
Tebak angka (1-100): 78
Selamat, tebakan Anda benar!
```

**Contoh Kode**
```cpp
#include <iostream>
using namespace std;

int main() {
    int angka_rahasia = 78;
    int tebakan;
    
    while (true) {
        cout << "Tebak angka (1-100): ";
        cin >> tebakan;
        
        if (tebakan < angka_rahasia) {
            cout << "Terlalu rendah" << endl;
        } else if (tebakan > angka_rahasia) {
            cout << "Terlalu tinggi" << endl;
        } else {
            cout << "Selamat, tebakan Anda benar!" << endl;
            break;
        }
    }
    
    return 0;
}
```

### 4. Mencetak Pola Segitiga Siku-Siku (Medium)

Buatlah program yang meminta pengguna memasukkan sebuah bilangan bulat N untuk tinggi segitiga. Program kemudian akan mencetak pola segitiga siku-siku yang terbuat dari karakter bintang * setinggi N.

Konsep: Penggunaan nested loop (loop bersarang). Loop luar untuk mengatur baris, dan loop dalam untuk mengatur jumlah bintang yang dicetak di setiap baris.

**Contoh Input:**
```
Masukkan tinggi segitiga: 5
```
**Contoh Output:**
```
*
**
***
****
*****
```

### 5. Input Data dan Cari Rata-rata (Hard)

Buatlah program yang meminta pengguna untuk memasukkan serangkaian bilangan positif secara terus-menerus. Perulangan akan berhenti ketika pengguna memasukkan angka -1. Setelah perulangan berhenti, program akan menghitung dan menampilkan nilai rata-rata dari semua bilangan yang telah dimasukkan (tidak termasuk angka -1).

Konsep: Penggunaan while(true) atau do-while untuk perulangan tak terbatas yang dihentikan oleh kondisi if dan break di dalamnya. Memerlukan variabel untuk menghitung jumlah (sum) dan banyaknya data (count).
**Contoh Interaksi:**
```
Masukkan bilangan (ketik -1 untuk berhenti): 10
Masukkan bilangan (ketik -1 untuk berhenti): 20
Masukkan bilangan (ketik -1 untuk berhenti): 30
Masukkan bilangan (ketik -1 untuk berhenti): -1
Rata-rata dari bilangan yang dimasukkan adalah: 20
```
**Contoh Kode**
```cpp
#include <iostream>
using namespace std;

int main() {
    double number, sum = 0;
    int count = 0;
    
    while (true) {
        cout << "Masukkan bilangan (ketik -1 untuk berhenti): ";
        cin >> number;
        
        if (number == -1) {
            break;
        }
        
        if (number > 0) {
            sum += number;
            count++;
        }
    }
    
    if (count > 0) {
        double average = sum / count;
        cout << "Rata-rata dari bilangan yang dimasukkan adalah: " << average << endl;
    } else {
        cout << "Tidak ada bilangan positif yang dimasukkan." << endl;
    }
    
    return 0;
}
```

## Soal
### 1. Cetak Angka Berurutan (Easy)

Buatlah program yang meminta pengguna memasukkan sebuah bilangan bulat N. Program akan mencetak semua angka dari 1 hingga N secara berurutan, masing-masing di baris baru.

Konsep: for loop sederhana dengan variabel iterator yang nilainya dicetak.
**Contoh Input:**
```
Masukkan bilangan N: 5
```
**Contoh Output:**
```
1
2
3
4
5
```
### 2. Menghitung Faktorial (Easy)

Buatlah program yang meminta pengguna memasukkan sebuah bilangan bulat positif N. Program akan menghitung nilai faktorial dari N (N!) dan menampilkannya. Faktorial adalah hasil perkalian semua bilangan bulat positif dari 1 sampai N. (Contoh: 5! = 5 * 4 * 3 * 2 * 1)

Konsep: for loop dengan variabel accumulator yang mengalikan nilai pada setiap iterasi.
**Contoh Input:**
```
Masukkan bilangan N: 5
```
**Contoh Output:**
```
Faktorial dari 5 adalah: 120
```

### 3. Validasi PIN ATM (Medium)

Buatlah program simulasi validasi PIN ATM. Tentukan sebuah pin_benar di dalam kode (misal: "123456"). Beri pengguna maksimal 3 kali kesempatan untuk memasukkan PIN.

- Jika PIN yang dimasukkan benar, cetak "PIN benar. Akses diberikan." dan hentikan program.
- Jika salah, cetak "PIN salah. Kesempatan tersisa: [jumlah]".
- Jika 3 kali salah, cetak "Kartu diblokir.".

Konsep: Menggunakan for loop dengan jumlah iterasi terbatas (3 kali) dan break untuk keluar dari loop jika kondisi benar terpenuhi sebelum loop selesai.

**Contoh Interaksi:**
```
Masukkan PIN: 111111
PIN salah. Kesempatan tersisa: 2
Masukkan PIN: 222222
PIN salah. Kesempatan tersisa: 1
Masukkan PIN: 123456
PIN benar. Akses diberikan.
```

### 4. Mencetak Pola Papan Catur (Medium)

Buatlah program yang meminta pengguna memasukkan sebuah bilangan bulat N. Program akan mencetak pola kotak-kotak berukuran N x N menggunakan karakter # dan       (spasi) yang polanya menyerupai papan catur.

Konsep: nested loop (loop bersarang) dengan tambahan logika if-else di dalamnya untuk menentukan karakter apa yang harus dicetak berdasarkan posisi baris dan kolom (ganjil/genap).
**Contoh Input:**
```
Masukkan ukuran papan: 5
```
**Contoh Output:**
```
# # #
 # # 
# # #
 # # 
# # #
```
### 5. Program Kasir Sederhana (Hard)

Buatlah program kasir yang akan terus meminta pengguna memasukkan harga barang satu per satu. Perulangan akan berhenti jika pengguna memasukkan angka 0. Setelah selesai, program akan menampilkan total belanjaan. Jika total belanjaan lebih dari Rp 100.000, berikan diskon 10% dan tampilkan harga akhir yang harus dibayar.

Konsep: Penggunaan while loop yang dihentikan oleh input spesifik. Menggabungkan accumulator untuk total harga dengan if-else di luar loop untuk menghitung diskon.
**Contoh Interaksi:**
```
Masukkan harga barang (ketik 0 untuk selesai): 50000
Masukkan harga barang (ketik 0 untuk selesai): 75000
Masukkan harga barang (ketik 0 untuk selesai): 0
Total Belanja: Rp 125000
Anda mendapat diskon 10%!
Harga yang harus dibayar: Rp 112500
```