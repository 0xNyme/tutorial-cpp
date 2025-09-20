---
sidebar_position: 1
---

# Basic Linux Commands

Berikut adalah perintah-perintah dasar Linux yang sering digunakan dalam pengembangan C++.

## Navigasi Directory

1. **pwd (Print Working Directory) menampilkan folder saat ini**
   ```bash
   $ pwd
   /home/user/projects
   ```

2. **ls (List Files) menampilkan seluruh list files**
   ```bash
   $ ls
   Documents  Downloads  program.cpp  output.exe
   
   # Dengan detail
   $ ls -l
   drwxr-xr-x 2 user user 4096 Sep 19 10:00 Documents
   drwxr-xr-x 2 user user 4096 Sep 19 10:00 Downloads
   -rw-r--r-- 1 user user  123 Sep 19 10:00 program.cpp
   -rwxr-xr-x 1 user user 8450 Sep 19 10:00 output.exe
   ```

3. **cd (Change Directory) merubah directory**
   ```bash
   $ cd Documents
   $ pwd
   /home/user/projects/Documents
   
   # Kembali ke directory sebelumnya
   $ cd ..
   ```

## File Management

1. **mkdir (Make Directory) membuat directory**
   ```bash
   $ mkdir projekC++
   $ ls
   Documents  Downloads  projekC++
   ```

2. **touch (Create Empty File) buat file lewat terminal**
   ```bash
   $ touch program.cpp
   $ ls
   Documents  Downloads  projekC++  program.cpp
   ```

3. **cp (Copy) mensalin file lewat terminal**
   ```bash
   $ cp program.cpp backup.cpp
   $ ls
   backup.cpp  program.cpp
   ```

4. **mv (Move/Rename) memindahkan atau ganti nama dengan terminal**
   ```bash
   $ ls
   
   $ mv program.cpp new_program.cpp
   $ ls
   backup.cpp  new_program.cpp
   ```

5. **rm (Remove) menghapus file**
   ```bash
   $ rm backup.cpp
   $ ls
   new_program.cpp
   ```

## File Content

1. **cat (View File Content)**
   ```bash
   $ cat program.cpp
   #include <iostream>
   using namespace std;
   
   int main() {
       cout << "Hello World!";
       return 0;
   }
   ```

2. **nano/vim (Text Editors)**
   ```bash
   $ nano program.cpp
   # Opens text editor
   ```

## System Commands

1. **clear (Clear Screen)**
   ```bash
   $ clear
   # Clears terminal screen
   ```

2. **history (Command History)**
   ```bash
   $ history
   1  pwd
   2  ls
   3  mkdir projekC++
   ```

## Compile & Run C++

1. **Compile Program**
   ```bash
   $ g++ program.cpp -o program
   ```

2. **Run Program**
   ```bash
   $ ./program
   Hello World!
   ```

## Tips Penting

- Gunakan Tab untuk auto-complete nama file/folder
- Gunakan ↑ dan ↓ untuk navigasi history command
- Selalu perhatikan current directory sebelum eksekusi command
- Gunakan `--help` untuk melihat opsi command