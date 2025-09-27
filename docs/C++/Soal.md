---
sidebar_position: 12
---

# Soal Latihan if else
if hanya di eksekusi jika bernilai true kondisi pengencekannya
## Contoh Soal
### Soal 1
Buatlah program yang meminta pengguna memasukkan sebuah bilangan bulat, lalu program akan menentukan dan mencetak apakah bilangan tersebut "Ganjil" atau "Genap".

Konsep : dalam kasus ini kita pake operator modulus (`%`) untuk mengecek sisa bagi yang dimana jika sisa bagi `1` akan bernilai ganjil dan jika sisa bagi `0` akan bernilai genap.\

**Contoh Input:**
```
Masukkan sebuah bilangan : 7
```
**Contoh Output**
```
Ganjil
```

**Contoh kode**
```cpp
#include <iostream>
using namespace std;

int main() {
    // deklarasi nilai untuk yang akan diuji apakah ganjil atau genap
    int number;
    // terima nilai dari input terminal
    cout << "Masukkan sebuah bilangan: ";
    cin >> number;
    
    // lakukan pengencekan menggunakan if else
    // alur
    // jika number = 4 dan 4 % 2 = 0 , maka apakah 0 == 0 ?
    // jika ya maka eksekusi baris program yang di awal if jika tidak pindah ke else
    if (number % 2 == 0) {
        cout << "Genap" << endl;
    } else {
        cout << "Ganjil" << endl;
    }
    
    return 0;
}
```
### Soal 2
Buatlah program yang meminta pengguna memasukkan usia mereka. Program kemudian akan mengkategorikan dan mencetak usia tersebut sebagai "Anak-anak" (di bawah 13), "Remaja" (13-19), atau "Dewasa" (20 ke atas).

Konsep: Penggunaan if, else if, dan else untuk beberapa kondisi.

**Contoh input :**
```bash 
Masukkan usia Anda: 15
```

**Contoh Output:**
```
Remaja
```
**Contoh Kode**
```cpp
#include <iostream>
using namespace std;

int main() {
    // variabel penampungan :v
    int age;
    cout << "Masukkan usia Anda: ";
    cin >> age;
    
    // cek perbandingan lu pada bisa baca lah ya :v
    if (age < 13) {
        cout << "Anak-anak" << endl;
    } else if (age >= 13 && age <= 19) {
        // kalo ini pake logika matematik
        // apakah nilai 14 >= 13 contoh 14 <= 19
        // nah disini nilai ny kan TRUE dan TRUE maka hasil TRUE 
        cout << "Remaja" << endl;
    } else {
        cout << "Dewasa" << endl;
    }
    
    return 0;
}
```

### Soal 3
Buatlah program kalkulator yang meminta pengguna memasukkan dua bilangan dan sebuah operator (`+`, `-`,`*`,`/`). Program akan melakukan operasi sesuai operator yang dimasukkan dan menampilkan hasilnya.

Konsep: Membandingkan karakter (char) dan menangani beberapa kasus operasi. disini pake `switch` kalo bingung tanya ai contoh pake `switch` gimana. capek aku ngetik :V gampang soalny

**Contoh Input:**
```
Masukkan bilangan pertama: 10
Masukkan operator (+, -, *, /): *
Masukkan bilangan kedua: 5
```
**Contoh Output:**
```
Hasil: 50
```

**Contoh Kode :**
```cpp
#include <iostream>
using namespace std;

int main() {
    // bisa pake double , int , atau float senyaman kalian
    double num1, num2, result;
    char op;
    
    cout << "Masukkan bilangan pertama: ";
    cin >> num1;
    cout << "Masukkan operator (+, -, *, /): ";
    cin >> op;
    cout << "Masukkan bilangan kedua: ";
    cin >> num2;
    
    switch (op) {
        case '+':
            result = num1 + num2;
            cout << "Hasil: " << result << endl;
            break;
        case '-':
            result = num1 - num2;
            cout << "Hasil: " << result << endl;
            break;
        case '*':
            result = num1 * num2;
            cout << "Hasil: " << result << endl;
            break;
        case '/':
        // di pembagian kita kasih pengecekan jika nilai !=
        // kenapa tidak sama dengan `!=` contoh apakah 1 != 0?
        // ya bener 1 != 0
        // cara baca `!=` itu tidak sama dengan ya
            if (num2 != 0) {
                result = num1 / num2;
                cout << "Hasil: " << result << endl;
            } else {
                cout << "Error: Pembagian dengan nol tidak diperbolehkan!" << endl;
            }
            break;
        default:
            cout << "Error: Operator tidak valid!" << endl;
    }
    
    return 0;
}
```
### Soal 4
Pengecekan Tahun Kabisat (Medium)

Buatlah program yang meminta pengguna memasukkan sebuah tahun. Program akan menentukan apakah tahun tersebut adalah "Tahun Kabisat" atau "Bukan Tahun Kabisat".

Aturan Tahun Kabisat:
- Habis dibagi 4, kecuali...
- Tahun yang habis dibagi 100.
- Namun, tahun yang habis dibagi 400 tetap dianggap tahun kabisat.

Konsep: Penggunaan if-else bersarang (nested) dengan logika kondisional yang kompleks (&& dan ||).

**Contoh Input:**
```
Masukkan tahun: 2000
```
**Contoh Output:**
```
Tahun Kabisat
```

**Contoh Kode:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int year;
    cout << "Masukkan tahun: ";
    cin >> year;
    
    if (year % 4 == 0) {
        if (year % 100 == 0) {
            if (year % 400 == 0) {
                cout << "Tahun Kabisat" << endl;
            } else {
                cout << "Bukan Tahun Kabisat" << endl;
            }
        } else {
            cout << "Tahun Kabisat" << endl;
        }
    } else {
        cout << "Bukan Tahun Kabisat" << endl;
    }
    
    return 0;
}
```

### Soal 5
Validasi Login Sederhana (Hard)

Buatlah program untuk memvalidasi login. Tentukan username dan password yang benar di dalam kode (misal: user_benar = "admin", pass_benar = "12345").

Program akan meminta input dari pengguna dan memberikan pesan berdasarkan kondisi berikut:
- Jika username dan password benar, cetak "Login Berhasil".
- Jika username salah, cetak "Username salah".
- Jika username benar tapi password salah, cetak "Password salah".

Konsep: Penggunaan if-else bersarang untuk memvalidasi dua input secara terpisah dan membandingkan tipe data string.

**Contoh Input:**
```
Masukkan username: admin
Masukkan password: 54321
```
**Contoh Output:**
```
Password salah
```
**Contoh Kode**
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string username, password;
    string user_benar = "admin";
    string pass_benar = "12345";
    
    cout << "Masukkan username: ";
    getline(cin, username); // sama aja kalo pake get line
    cout << "Masukkan password: ";
    getline(cin, password);
    
    if (username == user_benar) {
        if (password == pass_benar) {
            cout << "Login Berhasil" << endl;
        } else {
            cout << "Password salah" << endl;
        }
    } else {
        cout << "Username salah" << endl;
    }
    
    return 0;
}
```


## Soal latihan
### 1. Penentu Bilangan Positif, Negatif, atau Nol (Easy)

Buatlah program yang meminta pengguna memasukkan sebuah bilangan bulat. Program akan menentukan dan mencetak apakah bilangan tersebut "Positif", "Negatif", atau "Nol".

Konsep: Cek kondisi `>` (lebih besar dari), `<` (lebih kecil dari), dan `==` (sama dengan).

**Contoh Input:**
```
Masukkan sebuah bilangan: -5
```
**Contoh Output:**
```
Negatif
```

### 2. Konversi Nilai Menjadi Huruf (Easy)

Buatlah program untuk mengonversi nilai angka menjadi nilai huruf. Minta pengguna memasukkan nilai (0-100), lalu cetak hasilnya berdasarkan aturan:

- 85 - 100: `A`
- 75 - 84: `B`
- 65 - 74: `C`
- 50 - 64: `D`
- di bawah 50: `E`

Konsep: Rangkaian kondisi `if`, `else if`, `else` untuk rentang nilai.
**Contoh Input:**
```
Masukkan nilai Anda (0-100): 81
```
**Contoh Output:**
```
Nilai: B
```
### 3. Menghitung Luas Bangun Datar (Medium)

Buat program yang bisa menghitung luas. Pertama, tanya pengguna ingin menghitung luas apa: Persegi (P) atau Segitiga (S).

- Jika memilih 'P', minta input panjang sisi, lalu hitung dan tampilkan luasnya.

- Jika memilih 'S', minta input alas dan tinggi, lalu hitung dan tampilkan luasnya.

Konsep: Membaca input karakter, lalu menjalankan blok kode yang berbeda berdasarkan pilihan tersebut.

**Contoh Input:**
```
Pilih bangun datar (P/S): S
Masukkan alas: 10
Masukkan tinggi: 5
```
**Contoh Output:**
```
Luas Segitiga: 25
```

### 4. Kalkulator Harga Tiket Masuk (Medium)

Buat program untuk menentukan harga tiket masuk kebun binatang. Minta input usia dan hari kunjungan (misal: "Sabtu").
Aturan Harga:
- Usia di bawah 12 tahun (anak-anak): Rp 25.000
- Usia 12 tahun ke atas (dewasa): Rp 50.000
- Diskon Khusus: Khusus pada hari "Sabtu" atau "Minggu", tiket untuk anak-anak mendapat diskon 20%.

Konsep: if-else bersarang. Kondisi pertama mengecek usia, lalu di dalamnya ada kondisi lagi untuk mengecek hari.
**Contoh Input:**
```
Masukkan usia: 10
Masukkan hari kunjungan: Sabtu
```
**Contoh Output:**
```
Harga tiket: Rp 20000
```

### 5. Simulasi Mesin Penjual Minuman (Hard)

Buat program simulasi vending machine. Harga satu minuman adalah Rp 7.000. Stok minuman yang tersedia adalah 5 botol.
Program meminta pengguna memasukkan jumlah uang.
- Jika uang kurang dari harga, cetak "Uang tidak cukup".
- Jika uang cukup TAPI stok habis (0), cetak "Maaf, minuman habis" dan kembalikan uang.
- Jika uang cukup DAN stok masih ada, cetak "Transaksi berhasil, kembalian Anda: [jumlah]" dan kurangi stok sebanyak 1.

Konsep: if-else bersarang yang mengecek dua variabel (uang dan stok) untuk memberikan output yang spesifik di setiap kemungkinan kombinasi.
**Contoh Input:**
```
Harga minuman Rp 7000. Stok: 5
Masukkan uang Anda: 10000
```
**Contoh Output:**
```
Transaksi berhasil, kembalian Anda: 3000
```