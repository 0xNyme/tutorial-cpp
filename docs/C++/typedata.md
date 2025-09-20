---
sidebar_position: 5
---

# Tipe Data dalam C++

Berikut adalah penjelasan tentang tipe data dasar dalam C++ beserta implementasinya.

## 1. Integer (Bilangan Bulat)

```cpp
#include <iostream>
using namespace std;

int main() {
    int angka = 42;            // Regular integer
    short angkaKecil = 123;    // Short integer
    long angkaBesar = 123456;  // Long integer
    
    cout << "Int: " << angka << endl;
    cout << "Short: " << angkaKecil << endl;
    cout << "Long: " << angkaBesar << endl;
    
    return 0;
}
```

## 2. Float & Double (Bilangan Desimal)

```cpp
float nilaiFloat = 3.14f;      // 7 digit presisi
double nilaiDouble = 3.14159;  // 15 digit presisi

cout << "Float: " << nilaiFloat << endl;
cout << "Double: " << nilaiDouble << endl;
```

## 3. Character (Karakter)

```cpp
char huruf = 'A';              // Single character
char string[] = "Hello";       // Character array
string text = "Hello World";   // String object

cout << "Char: " << huruf << endl;
cout << "Char Array: " << string << endl;
cout << "String: " << text << endl;
```

## 4. Boolean

```cpp
bool benar = true;
bool salah = false;

cout << "Benar: " << benar << endl;  // Output: 1
cout << "Salah: " << salah << endl;  // Output: 0
```

## Ukuran Tipe Data

| Tipe Data | Ukuran (bytes) | Range |
|-----------|----------------|-------|
| char      | 1             | -128 to 127 |
| short     | 2             | -32,768 to 32,767 |
| int       | 4             | -2^31 to 2^31-1 |
| long      | 8             | -2^63 to 2^63-1 |
| float     | 4             | 3.4E-38 to 3.4E+38 |
| double    | 8             | 1.7E-308 to 1.7E+308 |
| bool      | 1             | true atau false |

## Contoh Program Lengkap

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    // Deklarasi variabel
    int umur = 25;
    float tinggi = 170.5f;
    string nama = "John Doe";
    bool aktif = true;
    char grade = 'A';
    
    // Output semua tipe data
    cout << "Nama: " << nama << endl;
    cout << "Umur: " << umur << " tahun" << endl;
    cout << "Tinggi: " << tinggi << " cm" << endl;
    cout << "Status Aktif: " << aktif << endl;
    cout << "Grade: " << grade << endl;
    
    return 0;
}
```

## Type Casting (Konversi Tipe Data)

```cpp
// Implicit casting
int x = 10;
double y = x;    // int ke double

// Explicit casting
double pi = 3.14;
int piInt = (int)pi;  // double ke int

cout << "Double: " << pi << endl;    // Output: 3.14
cout << "Int: " << piInt << endl;    // Output: 3
```

## Catatan Penting

- Pilih tipe data sesuai kebutuhan program
- Perhatikan range nilai yang akan disimpan
- Gunakan type casting dengan hati-hati
- String memerlukan `#include <string>`
- Boolean akan print sebagai 1 (true) atau 0 (false)