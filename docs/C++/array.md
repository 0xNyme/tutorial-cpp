---
sidebar_position: 9
---
# Array
so apa itu array 🔗 ? <br/>
array itu kalo di analogikan kayak loker sepatu yang tersusun rapi pake nomor urut dia bisa nampung banyak nilai di dalamny dengan kriteria tertentu seperti sepatu👟\
nah mirip array di programming juga gitu di bisa nyimpen nilai yang banyak berdasarkan tipe datanya.
```
tipe_data nama_var[ukuran_array];
```

## Cara Deklarasi Array

Array dapat dideklarasikan atau di buat dengan beberapa cara contohny:

```cpp
// Cara 1: Deklarasi array kosong
int numbers[5];  // Array dengan 5 elemen integer

// Cara 2: Deklarasi array dengan nilai awal
int scores[] = {90, 85, 78, 82, 95};  // Array akan otomatis berukuran 5

// Cara 3: Deklarasi array dengan ukuran dan nilai awal
int grades[5] = {85, 90, 75, 88, 92};
```

## Mengakses Elemen Array

Array menggunakan index yang dimulai dari 0:\
jika ingin mengakses angka 10 maka lokasi nya ada di index ke 0 seperti contoh dibawah

```cpp
int numbers[] = {10, 20, 30, 40, 50};
cout << numbers[0];  // Output: 10 (elemen pertama)
cout << numbers[4];  // Output: 50 (elemen terakhir)
```

## Mengubah Nilai Array
kalo mau ngubah nilai array ny kita bisa cari tau index ke berapa yang mau di ubah lalu isi dengan nilai yang ingin diganti seperti contoh dibawah ini
```cpp
int scores[3] = {75, 80, 85};
scores[1] = 95;  // Mengubah nilai index 1 dari 80 menjadi 95
```

## Array Multi-dimensi ( BONUS )

Array juga bisa memiliki lebih dari satu dimensi:

```cpp
// Array 2 dimensi (matrix 3x3)
int matrix[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

// Mengakses elemen array 2D
cout << matrix[0][0];  // Output: 1
cout << matrix[1][1];  // Output: 5
```

## Contoh Program Array

```cpp
#include <iostream>
using namespace std;

int main() {
    // Deklarasi array
    int nilai[5];
    
    // Input nilai
    for(int i = 0; i < 5; i++) {
        cout << "Masukkan nilai ke-" << i+1 << ": ";
        cin >> nilai[i];
    }
    
    // Tampilkan nilai
    cout << "\nNilai yang dimasukkan: ";
    for(int i = 0; i < 5; i++) {
        cout << nilai[i] << " ";
    }
    
    return 0;
}
```

## Tips Penggunaan Array

1. **Index Array**
   - Dimulai dari 0
   - Index terakhir = ukuran array - 1
   - Hindari mengakses index di luar batas array

2. **Ukuran Array**
   - Harus ditentukan saat deklarasi
   - Tidak bisa diubah setelah dideklarasi
   - Gunakan vector jika butuh ukuran dinamis

3. **Common Mistakes**
   - Mengakses index negatif
   - Mengakses index melebihi ukuran array
   - Lupa bahwa index dimulai dari 0

4. **Best Practices**
   - Selalu inisialisasi array
   - Gunakan loop untuk operasi pada array
   - Perhatikan batas array saat menggunakan loop

