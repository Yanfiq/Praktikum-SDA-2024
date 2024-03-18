# Analisis Kompleksitas

Pada semester pertama kita telah mempelajari bagaimana membuat algoritma untuk menyelesaikan suatu masalah. Namun, hal tersebut tidak sajalah cukup. Algoritma tidak saja harus benar (efektif), tetapi juga harus mangkus (efisien). Sehingga dapat dikatakan bahwa algoritma yang baik adalah algoritma yang mangkus. Kemangkusan suatu algoritma diukur dari sisi waktu (time) eksekusi serta penggunaan memori (space).

## 1 - Notasi Asimtotik

Terdapat beberapa jenis notasi asimtotik, tetapi kita hanya akan menggunakan dan membahas satu notasi saja, yaitu notasi Big-O. Big-O dipilih karena merupakan notasi yang paling populer dan paling banyak digunakan pada kalangan peneliti ilmu komputer. Notasi Big-O digunakan untuk mengkategorikan algoritma ke dalam fungsi yang menggambarkan batas atas (upper limit) dari pertumbuhan sebuah fungsi ketika masukan dari fungsi tersebut bertambah banyak.

| Fungsi Big-O | Nama       |
| ------------ | ---------- |
| O(1)         | Konstan    |
| O(log N)     | Logaritmik |
| O(N)         | Linear     |
| O(N log N)   | n log n    |
| O(N^2)       | Kuadratik  |
| O(N^m)       | Polinomial |
| O(N!)        | Faktorial  |

## 2 - Contoh Kriteria Kompleksitas

### O(1): Konstan

```cpp
// ...
cout << "Hello, world!" << endl;
// ...
```

Kompleksitas waktu dari sebuah fungsi (atau sekumpulan pernyataan) dianggap sebagai O(1) jika tidak mengandung perulangan, rekursi, dan pemanggilan ke fungsi lainnya yang memiliki waktu non-konstan. Dalam kode di atas "Hello, world!" mencetak hanya sekali di layar. Jadi, kompleksitas waktu adalah konstan: O(1) yaitu setiap kali jumlah waktu yang konstan diperlukan untuk mengeksekusi kode, apa pun sistem operasi atau konfigurasi mesin yang Anda gunakan.

### O(N): Linear

```cpp
// ...
int i, n = 8;
for (i = 1; i <= n; i++) {
   cout << "Hello, world!" << endl;
}
// ...
```

Kompleksitas waktu dari sebuah perulangan dianggap sebagai O(n) jika variabel-variabel perulangan ditambah/dikurangi dengan jumlah yang konstan. Sebagai contoh dalam kode di atas "Hello, world!" akan mencetak N kali. Jadi, kompleksitas waktu dari kode di atas adalah O(N).

### O(N^C): Polynomial

```cpp
// ...
for (int i = 1; i <= n; i++) {
    for(int j = 1; j <= n; j++) {
        cout << "Hey - I'm busy looking at: " + i + " and " + j << endl;
    }
}
// ...
```
Kompleksitas waktu dari perulangan bertumpuk sama dengan jumlah berapa kali statement terdalam dieksekusi. Sebagai contoh dalam kode diatas cout akan mencetak string sebanyak N kali untuk setiap iterasi pada loop terluar, dan loop terluar juga berjalan sebanyak N kali. Jadi, kompleksitas waktu dari kode diatas adalah kuadratik atau O(N^2). Jika nested loop berjumlah 3 maka kompleksitas waktunya adalah cubic atau O(N^3), demikian seterusnya.

### O (log N): Logaritmik

```cpp
// ...
int a = 0, i = N;
while (i > 0) {
	a += i;
	i /= 2;
}
// ...
```
Kompleksitas Waktu dari sebuah loop dianggap sebagai O(log n) jika variabel-variabel loop dibagi/dikalikan dengan jumlah yang konstan. Sebagai contoh dalam kode diatas variabel i dibagi 2 untuk setiap iterasinya.


### O(N log N): Linearitmik

```cpp
// ...
int i, j, k = 0;
for (i = 0; i <= N; i++) {
	for (j = 0; j <= N; j = j * 2) {
		// k = k + N / 2;
		cout << "Hey - I'm busy looking at: " + i + " and " + j << endl;
	}
}
// ...
```

Kompleksitas waktu Linearitmik merupakan kombinasi dari linear dan logaritmik. Dalam kode diatas, loop terluar memiliki kompleksitas O(n) karena variabel i ditambah dengan jumlah yang konstan, loop terdalam memiliki kompleksitas O(log n) karena variabel j dikali dengan jumlah yang konstan. Untuk setiap iterasi pada loop terluar, loop terdalam akan berjalan sebanyak log n sehingga kompleksitas waktu dari kode tersebut adalah O(n log n)


## 3 - Perbandingan Pertumbuhan Kompleksitas

![Gambar perbandingan kompleksitas](https://i.ytimg.com/vi/XiGedDZGOM8/hqdefault.jpg?sqp=-oaymwEXCNACELwBSFryq4qpAwkIARUAAIhCGAE=&rs=AOn4CLCoZ7k4wh3HCXJkQQ0zw_wgCF8ymw)

Pengembangan algoritma idealnya diusahakan mendapatkan kompleksitas O(1) atau O(logn). Sayangnya pada kenyataannya kita tidak akan selalu mendapatkan kompleksitas terbaik dalam merancang algoritma. Jika tidak dapat mencapai kompleksitas maksimal, hal terbaik yang dapat kita lakukan ketika mengembangkan solusi dari masalah adalah melihat apakah masalah yang ada dapat diselesaikan dengan algoritma yang ada terlebih dahulu, sebelum mengembangkan algoritma baru. Hal ini memastikan kita mendapatkan kompleksitas yang paling efisien sampai saat pengembangan solusi.

## 4 - Kesimpulan

Pada bagian ini kita telah mempelajari bagaimana melakukan analisa efisiensi algoritma dengan menggunakan notasi Big-O. Kita juga melihat bagaimana algoritma yang paling efisien memiliki kompleksitas O(1), dengan kompleksitas O(n!) sebagai kelas kompleksitas yang paling tidak efisien. Dengan mengerti efisiensi algoritma, diharapkan pembaca dapat memilih dan merancang algoritma yang sesuai dengan kebutuhan untuk menyelesaikan masalah.