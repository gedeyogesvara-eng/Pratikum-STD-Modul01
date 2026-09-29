# Praktikum-STD-Modul01
# <h1 align="center">Laporan Praktikum Modul 1 - Codeblocks IDE & Pengenalan Bahas C++ (Bagian Pertama)</h1>
<p align="center">Gede Yogi Yogesvara Dita Diasta - 109082500037</p>

## Dasar Teori
### A. Pengenalan C++
Bahasa C++ diciptakan oleh Bjarne Stroustrup di AT&T Bell Laboratories pada awal 1980 sebagai versi bahasa C yang dipercanggih dengan fasilitas kelas C with class.

### B. Tipe Data, Variabel, dan Input/Output
Dalam bahasa C++ data berdasarkan jenisnya dibagi ke dalam tipe data dasar yaitu bilangan bulat int, long, bilangan real float, double, karakter char, dan tak bertipe. Variabel digunakan untuk menyimpan nilai yang bisa berubah selama program berjalan, sedangkan konstanta dideklarasikan dengan kata const menyimpan nilai yang bersifat tetap tidak bisa dirubah. Untuk operasi Input dan Output standar bahasa C++ menggunakan file header <iostream>. Fungsi cout digunakan untuk mencetak teks atau nilai ke layar sedangkan fungsi cin digunakan untuk meminta input masukan dari pengguna.

### C. Operator, Kondisional, dan Perulangan
Bahasa C++ menyediakan berbagai macam operator di antaranya operator aritmatika +, -, *, /, %, operator pengerjaan =, +=, -=, serta operator logika &&, ||, !. Untuk menyelesaikan permasalahan yang membutuhkan pengambilan keputusan C++ menyediakan struktur kondisi seperti if, if-else, dan switch-case. Dan juga untuk mengefisienkan pengeksekusian sub program yang sama secara berulang kali digunakan struktur perulangan looping seperti for, while, dan do while yang akan terus berjalan selama kondisi batas perulangan masih terpenuhi.

## Guided 

### 1. Latihan Pengenalan Output

```C++
#include <iostream>
using namespace std;

int main() {
    cout << "Hello saya belajar c++ anjay mabar" << endl;
    return 0;
}
```
Program di atas merupakan pengenalan dasar sintaks C++ untuk melakukan cetak teks ke layar output menggunakan perintah cout

### 2. Latihan Fungsi Input

```C++
#include <iostream>
using namespace std;

int main() {
    int inp;
    cin >> inp;
    cout << "Nilai = " << inp;
    return 0;
}
```
Program ini cara menggunakan fungsi cin untuk meminta masukan input berupa angka dari pengguna, menyimpannya ke dalam variabel inp, lalu mencetaknya kembali ke layar menggunakan cout.

### 3. Latihan Operasi Aritmatika

```C++
#include <iostream>
using namespace std;

int main() {
    int w, x, y;
    float z;

    x = 7;
    y = 3;
    w = 1;

    z = (float) (x + y) / (y + w);
    cout << "z = " << z << endl;
    return 0;
}
```
Program ini menunjukkan penggunaan beberapa variabel, inisialisasi nilai, dan juga operasi aritmatika dasar di dalam bahasa C++. Terdapat juga penggunaan type casting float untuk mengonversi hasil perhitungan bilangan bulat integer menjadi bilangan pecahan float.

## Unguided 

### 1. Buatlah program yang menerima input-an dua buah bilangan betipe float, kemudian memberikan output-an hasil penjumlahan, pengurangan, perkalian, dan pembagian dari dua bilangan tersebut.

```C++
#include <iostream>
using namespace std;

int main() {
    float a, b;
    cout << "Masukkan 2 bilangan : ";
    cin >> a >> b;

    cout << "Hasil penjumlahan " << a << " + " << b << " = " << a + b << endl;
    cout << "Hasil pengurangan " << a << " - " << b << " = " << a - b << endl;
    cout << "Hasil perkalian " << a << " x " << b << " = " << a * b << endl;
    cout << "Hasil pembagian " << a << " : " << b << " = " << a / b << endl;

    return 0;
}
```
### Output Unguided 1 :
![Screenshot Output Unguided 1](https://github.com/gedeyogesvara-eng/Pratikum-STD-Modul01/blob/main/modul-1/Screenshot-Soal1.png)

penjelasan unguided 1
Program ini menggunakan tipe data float untuk menampung dua variabel input a dan b berupa bilangan desimal. Program kemudian menerapkan operator aritmatika dasar di C++ yaitu penambahan +, pengurangan -, perkalian *, dan pembagian / untuk memproses kedua bilangan masukan tersebut. Lalu operasi aritmatika dieksekusi secara langsung di dalam perintah output cout sehingga tidak memerlukan variabel tambahan dan hasilnya langsung dicetak ke layar secara berurutan.

### 2. Buatlah sebuah program yang menerima masukan angka dan mengeluarkan output nilai angka tersebut dalam bentuk tulisan. Angka yang akan di-input-kan user adalah bilangan bulat positif mulai dari 0 s.d 100.

```C++
#include <iostream>
using namespace std;

int main() {
    int a;

    cout << "Masukkan angka : ";
    cin >> a;

    string namaangka[] = {"nol", "satu", "dua", "tiga", "empat", "lima", "enam", "tujuh", "delapan", "sembilan", "sepuluh", "sebelas", "belas", "puluh", "seratus"};

    if (a >= 0 && a <= 10) {
        cout << a << " : " << namaangka[a] << endl;
    } else if (a == 11) {
        cout << a << " : " << namaangka[11] << endl;
    } else if (a > 11 && a < 20) {
        cout << a << " : " << namaangka[a - 10] << " belas" << endl;
    } else if (a >= 20 && a < 100) {
        int puluhan = a / 10;
        int satuan = a % 10;
        cout << a << " : " << namaangka[puluhan] << " puluh";
        if (satuan != 0) {
            cout << " " << namaangka[satuan];
        }
        cout << endl;
    } else if (a == 100) {
        cout << a << " : " << namaangka[14] << endl;
    } else {
        cout << "Angka tidak valid" << endl;
    }

    return 0;
}
```
### Output Unguided 2 :
![Screenshot Output Unguided 2](https://github.com/gedeyogesvara-eng/Pratikum-STD-Modul01/blob/main/modul-1/Screenshot-Soal2.png)

penjelasan unguided 2
Program ini berfungsi untuk mengonversi angka bilangan bulat 0 sampai 100 menjadi teks ejaan. Untuk efisiensi program menggunakan struktur array string bernama namaangka yang menyimpan kosa kata angka dasar. Program menggunakan struktur kontrol percabangan if else if else untuk memilah rentang angka. Khusus untuk angka puluhan 20 sampai 99, program menerapkan operator aritmatika pembagian / untuk mendapatkan nilai puluhan dan operator modulus % untuk mendapatkan nilai satuan, lalu menggabungkannya dengan elemen array untuk mencetak ejaan yang tepat secara dinamis.

### 3. Buatlah program yang dapat memberikan input dan output berupa pola cermin susunan angka yang mengecil ke tengah dan dipisahkan oleh tanda bintang *.

```C++
#include <iostream>
using namespace std;

int main() {
    int a;

    cout << "input : ";
    cin >> a;
    cout << endl;

    for (int i = a; i >= 1; i--) {
        for (int k = 1; k <= a - i; k++) {
            cout << "  ";
        }
        for (int j = i; j >= 1; j--) {
            cout << " " << j ;
        }
            for (int i = a; i <= a; i++) {
                  cout << " *";
        }
            for (int j = 1; j <= i; j++) {
            cout << " " << j ;
        }
        cout << endl;
    }
            for (int k = 1; k <= a ; k++) {
            cout << "  ";
        }
     cout << " *";
}
```
### Output Unguided 3 :
![Screenshot Output Unguided 3](https://github.com/gedeyogesvara-eng/Pratikum-STD-Modul01/blob/main/modul-1/Screenshot-Soal3.png)

penjelasan unguided 3
Program ini berfungsi untuk mencetak pola susunan angka berbentuk segitiga terbalik dengan efek cermin. Program menggunakan perulangan didalam perulangan bertipe for. Loop utama bagian paling luar untuk perpindahan baris dari atas ke bawah. Di dalam loop utama ditambahkan beberapa loop untuk mengelola elemen di tiap barisnya secara spesifik, antara lain loop untuk mencetak spasi agar teks bergeser ke kanan membentuk pola piramida, loop untuk mencetak angka yang menurun decrement, loop batas tunggal untuk mencetak bintang pembatas, dan loop untuk mencetak angka menaik increment. Di luar dari keseluruhan proses tersebut, terdapat loop tambahan terakhir untuk mengatur spasi posisi satu bintang penutup di baris paling bawah.

## Kesimpulan
Dari praktikum modul 1 ini memplajari dasar-dasar pemrograman menggunakan bahasa C++. Praktikum ini mencakup pengenalan struktur dasar program, deklarasi variabel beserta tipe datanya seperti int, float, dan string dan juga penerapan operasi masukan cin dan keluaran cout standar. Lalu berhasil diimplementasikan juga penggunaan berbagai operator matematika dasar, struktur kontrol pengambilan keputusan kondisional if-else, dan perulangan looping berupa nested for untuk memecahkan berbagai permasalahan.

## Referensi
[1] Telkom University. (2026). *Modul 1: Code Blocks IDE & Pengenalan Bahasa C++ (Bagian Pertama)*. Modul Praktikum Struktur Data. Fakultas Informatika, Telkom University Purwokerto.
<br>[2] Stroustrup, B. (2013). *The C++ Programming Language* (4th ed.). Addison-Wesley Professional.
