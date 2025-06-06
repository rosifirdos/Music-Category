# Music Library Organizer

## Deskripsi
Music Library Organizer adalah aplikasi sederhana berbasis Python untuk mengelola koleksi musik secara hierarkis menggunakan struktur data **pohon n-ary**. Program ini memungkinkan pengguna untuk mengelompokkan lagu berdasarkan **genre**, **artis**, dan **album**, serta melakukan operasi seperti menambahkan lagu, menghapus lagu, dan menampilkan statistik jumlah lagu per genre. Aplikasi ini dirancang untuk memberikan struktur yang rapi dan mudah dipahami, mirip dengan sistem pengelompokan produk pada platform e-commerce.

## Fitur
- **Hierarki Musik**: Mengelompokkan lagu dalam struktur pohon dengan empat level: Genre → Artist → Album → Song.
- **Penambahan Lagu**: Menambahkan lagu baru dengan validasi untuk mencegah duplikasi (case-insensitive).
- **Penghapusan Lagu**: Menghapus lagu tertentu dari album berdasarkan judul.
- **Statistik**: Menampilkan jumlah lagu per genre.
- **Tampilan Hierarki**: Menampilkan koleksi musik dalam format berindentasi yang jelas.

## Struktur Data
Program menggunakan **pohon n-ary** (general tree) dengan karakteristik berikut:
- **Level Hierarki**:
  1. **Genre**: Kategori utama (misalnya, Pop Punk, Hardcore).
  2. **Artist**: Nama artis dalam genre tertentu (misalnya, Green Day, Defy).
  3. **Album**: Album milik artis (misalnya, American Idiot, Who Suffer?).
  4. **Song**: Lagu dengan atribut judul, durasi, dan tahun rilis.
- Setiap node dapat memiliki banyak anak (n-ary), mendukung banyak artis per genre, banyak album per artis, dan banyak lagu per album.
- Validasi duplikasi memastikan tidak ada entitas (genre, artis, album, lagu) yang duplikat dalam hierarki.

## Prasyarat
- Python 3.12 atau lebih tinggi.
- Lingkungan Jupyter Notebook (opsional, untuk menjalankan file `kategori_musik.ipynb`).
- Tidak ada dependensi eksternal.

## Cara Menjalankan
1. **Jalankan di Jupyter Notebook**:
   - Buka file `kategori_musik.ipynb` di Jupyter Notebook:
     ```bash
     jupyter notebook kategori_musik.ipynb
     ```
   - Jalankan semua sel kode untuk melihat output hierarki musik, penghapusan lagu, dan statistik.

2. **Jalankan sebagai Skrip Python**:
   - Salin kode dari sel utama di `kategori_musik.ipynb` ke file Python (misalnya, `music_library.py`).
   - Jalankan file:
     ```bash
     python music_library.py
     ```
   - Output akan menampilkan hierarki koleksi musik, hasil penghapusan lagu, dan statistik jumlah lagu per genre.

## Contoh Output
```plaintext
Koleksi Musik Awan:
Genre: Pop Punk (2 songs)
  Artist: Green Day
    Album: American Idiot
      Song: Jesus of Suburbia - 9:08, 2004
  Artist: Pee Wee Gaskins
    Album: A Youth Not Wasted
      Song: Sassy Girl - 3:34, 2016
Genre: Hardcore (3 songs)
  Artist: Kenya
    Album: Trust No One
      Song: Sanity - 3:03, 2024
  Artist: Defy
    Album: Who Suffer?
      Song: Be Gone! - 1:47, 2022
      Song: Conquer - 1:47, 2022

Menghapus lagu 'Conquer' dari album 'Who Suffer?':
Genre: Pop Punk (2 songs)
  Artist: Green Day
    Album: American Idiot
      Song: Jesus of Suburbia - 9:08, 2004
  Artist: Pee Wee Gaskins
    Album: A Youth Not Wasted
      Song: Sassy Girl - 3:34, 2016
Genre: Hardcore (2 songs)
  Artist: Kenya
    Album: Trust No One
      Song: Sanity - 3:03, 2024
  Artist: Defy
    Album: Who Suffer?
      Song: Be Gone! - 1:47, 2022

Statistik Jumlah Lagu per Genre:
Genre: Pop Punk - 2 songs
Genre: Hardcore - 2 songs
```

## Struktur Proyek
```
music-library-organizer/
├── kategori_musik.ipynb  # File utama berisi kode aplikasi
└── README.md             # Dokumentasi proyek
