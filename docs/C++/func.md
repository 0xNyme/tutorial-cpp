---
sidebar_position: 10
---
# Fungsi atau `Function`

Fungsi (function) adalah blok kode terorganisir yang dapat digunakan kembali untuk melakukan sebuah tugas atau aksi tertentu. Anggap saja fungsi seperti "resep" dalam program: kamu menuliskannya sekali, lalu bisa "memasaknya" (memanggilnya) kapan pun kamu butuh tanpa harus menulis ulang semua langkahnya.

## Struktur Dasar Fungsi
- tipe return itu tipe data contoh `int`, `float` , `double` , dan kawan kawanny.
- nama fungsi nanti yang akan dipanggil di baris program lain
- return nilai sesuai dengan data type awal kalo awalny `int` ya return nya `int` juga

```cpp
tipe_return nama_fungsi(parameter) {
    // kode yang akan dijalankan
    return nilai;  // opsional, sesuai tipe_return
}
```

## Contoh Fungsi Sederhana

```cpp
int tambah(int a, int b) {
    return a + b;
}

void sayHello() {
    cout << "Hello World!" << endl;
}
```

## Jenis-jenis Fungsi

1. **Fungsi dengan Return Value**
```cpp
int hitungLuas(int panjang, int lebar) {
    return panjang * lebar;
}

// Cara pakai
int luas = hitungLuas(5, 3);  // luas = 15
```

2. **Fungsi Void (Tanpa Return)**
    - fungsi ini ada buat execute logic aja gk mengembalikan nilai sama sekali
```cpp
void tampilkanNilai(string nama, int nilai) {
    cout << nama << " mendapat nilai " << nilai << endl;
}

// Cara pakai
tampilkanNilai("John", 85);
```

3. **Fungsi dengan Parameter Default**
- ini maksud ny nilai bawaan atau defaul dari parameter itu sendiri semisal parameter ny gk di isi bakal pake bawaanny 
```cpp
void sapaPengguna(string nama = "User") {
    cout << "Halo " << nama << "!" << endl;
}

// Cara pakai
sapaPengguna();        // Output: Halo User!
sapaPengguna("John");  // Output: Halo John!
```

## Contoh Program Lengkap

```cpp
#include <iostream>
using namespace std;

// Deklarasi fungsi
int tambah(int a, int b);
int kurang(int a, int b);
void tampilkanHasil(string operasi, int hasil);

int main() {
    int x = 10, y = 5;
    
    // Memanggil fungsi
    int hasilTambah = tambah(x, y);
    int hasilKurang = kurang(x, y);
    
    // Menampilkan hasil
    tampilkanHasil("Pertambahan", hasilTambah);
    tampilkanHasil("Pengurangan", hasilKurang);
    
    return 0;
}

// Definisi fungsi
int tambah(int a, int b) {
    return a + b;
}

int kurang(int a, int b) {
    return a - b;
}

void tampilkanHasil(string operasi, int hasil) {
    cout << "Hasil " << operasi << ": " << hasil << endl;
}
```

## Tips Penggunaan Fungsi

1. **Penamaan Fungsi**
   - Gunakan nama yang jelas dan deskriptif
   - Ikuti konvensi penamaan (camelCase atau snake_case)
   - Nama harus menggambarkan apa yang dilakukan fungsi

2. **Parameter**
   - Tentukan tipe data parameter dengan tepat
   - Gunakan parameter default jika diperlukan
   - Perhatikan urutan parameter

3. **Return Value**
   - Sesuaikan tipe return dengan kebutuhan
   - Gunakan void jika tidak perlu mengembalikan nilai
   - Pastikan semua path memiliki return (jika bukan void)

4. **Best Practices**
   - Satu fungsi sebaiknya melakukan satu tugas spesifik
   - Hindari fungsi yang terlalu panjang
   - Dokumentasikan fungsi dengan komentar jika perlu
   - Deklarasikan fungsi sebelum digunakan