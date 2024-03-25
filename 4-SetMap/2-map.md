# 2 - Map

## Konsep Map

Map (atau **pemetaan**) adalah struktur data yang *memetakan* suatu nilai ke nilai lain. Sederhananya, suatu nilai yang berada dalam dalam map berkorespondensi dengan nilai lain (bisa dengan tipe data yang berbeda).

Dalam praktiknya, map sering digunakan sebagai solusi pengganti indeks berbasis integer pada array (misalnya diganti menjadi indeks berbasis string).

Seperti halnya set, map juga umumnya direpresentasikan dalam bentuk binary search tree supaya proses menambah, menghapus, dan mencari elemen bisa dilakukan seefisien mungkin (kompleksitas O(log N)).

Dalam C++, struktur data map terletak dalam header `<map>`.

## Deklarasi

Mendeklarasikan map yang memetakan string ke suatu struct `Mahasiswa`:
```c++
std::map<std::string, Mahasiswa> data_mhs;
```

## Operasi

### Assignment

Mengaitkan mahasiswa dengan indeks **L0123456** dengan obyek dari struct pada map `data_mhs`:
```c++
Mahasiswa mhs;
mhs.nama = "Rizal Basshead";
mhs.prodi = "Informatika";
mhs.angkatan = 2025;
data_mhs["L0123456"] = mhs;
```

### Access

Mendapatkan obyek mahasiswa dengan indeks **L0123456** dari map `data_mhs`:
```c++
Mahasiswa mhs = data_mhs["L0123456"];
std::cout << "Nama: " << mhs.nama << std::endl;
std::cout << "Prodi: " << mhs.prodi << std::endl;
std::cout << "Angkatan: " << mhs.angkatan << std::endl;
```

Untuk memaninpulasi obyek mahasiswa dengan indeks **L0123456** dalam map `data_mhs`:
```c++
data_mhs["L0123456"].nama = "Farhan Treble";

// atau menggunakan reference:

Mahasiswa &mhs = data_mhs["L0123456"];
mhs.nama = "Farhan Treble";
```

Mengecek apakah mahasiswa dengan indeks **L0123456** berada dalam `data_mhs`:
```c++
if (data_mhs.count("L0123456") == 1) {
    std::cout << "L0123456 merupakan mahasiswa UNS" << std::endl;
} else {
    std::cout << "L0123456 bukan merupakan mahasiswa UNS" << std::endl;
}
```

### Removal

Menghapus **L0123456** dari `data_mhs`:
```c++
data_mhs.erase("L0123456");
```

### Iteration

Iterasi seluruh elemen `data_mhs`:
```c++
for (
    std::map<std::string, Mahasiswa>::iterator it = data_mhs.begin();
    it != data_mhs.end();
    ++it
) {
    std::cout << it->first << ": " << it->second.nama << std::endl;
}
```

## Selengkapnya

- [C++ Map](https://en.cppreference.com/w/cpp/container/map)
