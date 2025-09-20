---
sidebar_position: 7
---

# If Statement (Percabangan) dalam C++

Percabangan menggunakan if statement memungkinkan program untuk mengeksekusi kode berdasarkan kondisi tertentu.

## 1. If Sederhana

```cpp
if (kondisi) {
    // kode yang dijalankan jika kondisi bernilai true
}
```

Contoh:
```cpp
int nilai = 75;

if (nilai >= 70) {
    cout << "Anda Lulus!" << endl;
}
```

## 2. If-Else

```cpp
if (kondisi) {
    // kode jika kondisi true
} else {
    // kode jika kondisi false
}
```

Contoh:
```cpp
int umur = 15;

if (umur >= 17) {
    cout << "Boleh membuat SIM" << endl;
} else {
    cout << "Belum boleh membuat SIM" << endl;
}
```

## 3. If-Else If-Else

```cpp
if (kondisi1) {
    // kode jika kondisi1 true
} else if (kondisi2) {
    // kode jika kondisi2 true
} else {
    // kode jika semua kondisi false
}
```

Contoh:
```cpp
int nilai = 85;

if (nilai >= 90) {
    cout << "Nilai A" << endl;
} else if (nilai >= 80) {
    cout << "Nilai B" << endl;
} else if (nilai >= 70) {
    cout << "Nilai C" << endl;
} else {
    cout << "Nilai D" << endl;
}
```

## 4. Nested If (If Bersarang)

```cpp
if (kondisi1) {
    if (kondisi2) {
        // kode jika kondisi1 dan kondisi2 true
    }
}
```

Contoh:
```cpp
int usia = 25;
bool punya_sim = true;

if (usia >= 17) {
    if (punya_sim) {
        cout << "Boleh mengemudi" << endl;
    } else {
        cout << "Harus membuat SIM dulu" << endl;
    }
} else {
    cout << "Belum cukup umur untuk mengemudi" << endl;
}
```

## 5. Operator Logika dalam If

```cpp
if (kondisi1 && kondisi2) {    // AND
    // kode jika kedua kondisi true
}

if (kondisi1 || kondisi2) {    // OR
    // kode jika salah satu kondisi true
}
```

Contoh:
```cpp
int nilai = 85;
bool hadir = true;

if (nilai >= 75 && hadir) {
    cout << "Lulus" << endl;
} else {
    cout << "Tidak Lulus" << endl;
}
```

## 6. Kombinasi AND dalam If Statement

Menggunakan operator `&&` untuk menggabungkan beberapa kondisi yang harus bernilai true secara bersamaan.

```cpp
#include <iostream>
using namespace std;

int main() {
    int nilai;
    int kehadiran;
    
    cout << "Masukkan nilai: ";
    cin >> nilai;
    cout << "Masukkan persentase kehadiran: ";
    cin >> kehadiran;
    
    // Cek kelulusan berdasarkan nilai DAN kehadiran
    if (nilai >= 75 && kehadiran >= 80) {
        cout << "Selamat, Anda LULUS!" << endl;
        if (nilai >= 90) {
            cout << "Anda mendapat nilai A" << endl;
        }
    } else {
        cout << "Maaf, Anda TIDAK LULUS" << endl;
        if (nilai < 75) {
            cout << "Nilai kurang dari 75" << endl;
        }
        if (kehadiran < 80) {
            cout << "Kehadiran kurang dari 80%" << endl;
        }
    }
    
    return 0;
}
```

### Contoh Lain Kombinasi AND

```cpp
// Cek eligibilitas kredit
int usia, penghasilan;
bool memilikiPekerjaan;

cout << "Masukkan usia: ";
cin >> usia;
cout << "Masukkan penghasilan per bulan: ";
cin >> penghasilan;
cout << "Memiliki pekerjaan tetap (1/0): ";
cin >> memilikiPekerjaan;

if (usia >= 21 && penghasilan >= 5000000 && memilikiPekerjaan) {
    cout << "Anda eligible untuk mengajukan kredit" << endl;
} else {
    cout << "Maaf, Anda belum eligible untuk kredit" << endl;
}
```

### Tips Penggunaan AND

- Semua kondisi harus terpenuhi (true) agar blok kode dijalankan
- Urutan kondisi bisa mempengaruhi performa (short-circuit evaluation)
- Gunakan tanda kurung untuk memperjelas urutan evaluasi
- Bisa dikombinasikan dengan OR (`||`) untuk kondisi lebih kompleks

Contoh dengan kurung:
```cpp
if ((nilai >= 80 && kehadiran >= 90) || (nilai >= 95 && kehadiran >= 75)) {
    cout << "Anda lulus dengan baik" << endl;
}
```

## Catatan Tambahan untuk AND

- Evaluasi berhenti saat menemui false (short-circuit)
- Lebih baik letakkan kondisi yang sering false di awal
- Bisa digabung dengan nested if untuk logic yang kompleks
- Perhatikan prioritas operator saat menggabungkan AND dan OR

## Contoh Program Lengkap

```cpp
#include <iostream>
using namespace std;

int main() {
    int nilai;
    cout << "Masukkan nilai: ";
    cin >> nilai;
    // cek nilai ny apakah lebih besar dari yang di inginkan
    if (nilai >= 90) {
        cout << "Nilai A" << endl;
        cout << "Excellent!" << endl;
    } else if (nilai >= 80) {
        cout << "Nilai B" << endl;
        cout << "Good job!" << endl;
    } else if (nilai >= 70) {
        cout << "Nilai C" << endl;
        cout << "Keep trying!" << endl;
    } else {
        cout << "Nilai D" << endl;
        cout << "Please study harder!" << endl;
    }
    
    return 0;
}
```

## Catatan Penting

- Gunakan kurung kurawal `{}` untuk blok kode yang lebih dari satu baris
- Kondisi dalam if harus menghasilkan nilai boolean (true/false)
- Perhatikan operator perbandingan yang digunakan (`==`, `!=`, `>`, `<`, `>=`, `<=`)
- Nested if sebaiknya tidak terlalu dalam untuk menjaga keterbacaan kode
- Gunakan operator logika (`&&`, `||`, `!`) untuk kombinasi kondisi