# Tugas Praktikum List, Stack, & Queue

NOTE

1. Gunakan bahasa **C++**
2. Kumpulkan semua source code pada assignment Google Classroom **(jangan di-ZIP)**, diberi format: **NIM_Nama_PSDA01_NomorSoal.cpp**, 

   misal apabila mengumpulkan nomor 1 : **L0122081_JassonFranklynWang_PSDA01_1.cpp**

## No. 1 - List

Ikuti langkah-langkah berikut **(bobot: 40%)**:

1. Buatlah list untuk menyimpan data berupa sekumpulan string: **Rambutan**, **Jambu**, **Jeruk**, **Melon**, **Semangka**, **Durian**
2. Bagi list menjadi 2 bagian (list1 dan list2), dengan isi list1 : **Rambutan**, **Jambu**, **Jeruk** dan isi list2 : **Melon**, **Semangka**, **Durian**
3. Lalu hapus **Jambu** dari list1 dan **Durian** dari list2
4. Setelah itu, tampilkan isi dari kedua list tersebut

Contoh Output: 
```
Seluruh List:
Rambutan
Jambu
Jeruk
Melon
Semangka
Durian
List 1:
Rambutan
Jeruk
List 2:
Melon
Semangka
```

Anda boleh menggunakan array list (std::vector) ataupun linked list (std::list)

## No. 2 - Stack

Simulasikan fitur browsing history menggunakan stack **(bobot: 30%)**:

Ikutilah langkah-langkah berikut:
1. Buatlah stack untuk menyimpan history.
2. Buatlah 2 fungsi, visit(std::string) untuk mengunjungi sebuah website dan back() untuk kembali ke halaman sebelumnya.

Contoh penggunaan fungsi:
```
- visit("google.com")
- visit("instagram.com")
- visit("github.com")
- back()
- back()
- visit("stackoverflow.com")
```

Contoh output (urut):
```
- Mengunjungi google.com
- Mengunjungi instagram.com
- Mengunjungi github.com
- Mengunjungi instagram.com
- Mengunjungi google.com
- Mengunjungi stackoverflow.com
```

Nilai tambahan jika menambahkan fungsi forward() untuk mengunjungi halaman yang dikunjungi setelah halaman x. Anda boleh menggunakan stack lebih dari 1.

## No. 3 - Queue

Selesaikan permasalahan di bawah menggunakan queue (dan stack) **(bobot: 30%)**:

Komputer Pak Dengklek memiliki berbagai macam perintah:

|Perintah|Deskripsi|
|--|--|
|PUSH 0|Memasukkan angka 0 ke atas stack|
|PUSH 1|Memasukkan angka 1 ke atas stack|
|TOP|Menampilkan angka yang berada di atas stack|
|POP|Mengeluarkan angka yang berada di atas stack|

Komputer tersebut bekerja dengan cara menerima input kemudian memasukkannya ke dalam queue, lalu dieksekusi oleh mesin dengan cara membaca isi queue tersebut. Dengan demikian, apabila komputer pak dengklek menerima perintah (urut):

- PUSH 0
- PUSH 0
- TOP
- PUSH 1
- TOP
- POP
- POP
- TOP

Maka akan menampilkan output berupa:
```
010
```

Buatlah program yang mensimulasikan permasalahan tersebut menggunakan queue (dan stack)! Anda bebas memasukkan perintah apapun ke dalam queue dan melalui manapun (melalui source code atau user input atau file input).
