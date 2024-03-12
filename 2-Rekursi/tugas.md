# Tugas Praktikum Rekursi

NOTE

1. Gunakan bahasa **C++**
2. Kumpulkan source code pada assignment Google Classroom, diberi format: **NIM_Nama_PSDA02.cpp**, contoh : **L0122081_JassonFranklynWang_PSDA02.cpp**

### Soal: Deret Fibonacci

Tuliskan sebuah fungsi untuk menghitung angka Fibonacci ke-n menggunakan rekursi.

Deret Fibonacci adalah deret angka di mana setiap angka adalah jumlah dari dua angka sebelumnya, dimulai dari 0 dan 1. Dalam istilah matematika, deret ini didefinisikan oleh Relasi perulangan:
```
F(n) = F(n-1) + F(n-2)
```
dengan nilai awal:
```
F(0) = 0, F(1) = 1
```
Tugas Anda adalah mengimplementasikan fungsi rekursif ```int fibonacci(int n)``` yang mengembalikan angka Fibonacci ke-n berdasarkan relasi perulangan.

Contoh:
input: 5
output: 5

input: 10
output: 55