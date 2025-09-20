---
sidebar_position: 3
---

# COUT (Console Output)

`cout` itu standard output dalam c++ yang digunakan untuk menampilan sebuah nilai ke dalam console atau terminal kalian . cout juga merupakan bagian dari library iostream.

## Basic Syntax

```cpp
cout << value;
```

## Examples

```cpp
#include <iostream>
using namespace std;

int main() {
    // output "Hello World"
    cout << "Hello World";

    // Output dengan angka
    int num = 42;
    cout << "The number is: " << num;

    // Output with multiple items
    // bisa di chained juga
    string name = "John";
    int age = 25;
    cout << "Name: " << name << ", Age: " << age;

    // Output dengan baris baru
    cout << "First line" << endl;
    cout << "Second line" << "\n";

    return 0;
}
```

## penggunaan umum

1. **Teks Output**
   ```cpp
   cout << "Hello World";
   ```

2. **Angka Output**
   ```cpp
   cout << 42;
   ```

3. **Variabel Output**
   ```cpp
   int x = 10;
   cout << x;
   ```

4. **jika nilai nya output nya banyak**
   ```cpp
   cout << "x = " << x << endl;
   ```

## Important Notes

- selalu sertakan library `<iostream>` ketika menggunakan cout
- gunakan `endl` atau `\n` untuk baris baru
- dapat chained dengan banyak `<<` operators
- merupakan bagian dari `std` namespace