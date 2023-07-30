# Proyek SQL Music

Selamat datang di Proyek SQL Menarik! Proyek ini dirancang untuk memberikan pengalaman belajar yang menarik tentang SQL dan penggunaannya dalam manajemen database.

## Daftar Isi

- [Schema Diagram](#schema-diagram)
- [Pertanyaan Bagian 1](#pertanyaan-bagian-1)
- [Pertanyaan Bagian 2](#pertanyaan-bagian-2)


## Schema Diagram

<!-- Project Header -->
<div align="center">
  <img src="https://github.com/Royjihan21/Data_Latihan_SQL_1_Music/blob/main/schema_diagram.png">
</div>

## Pertanyaan Bagian 1

1. Siapa karyawan paling senior berdasarkan jabatan.
  - **Query**
    ***
      select title,last_name,levels 
      from sql_port_1_music.employee 
      order by levels desc 
      limit 1;

  - **Penjelasan Query**
    ***
    Query di atas adalah sebuah perintah SQL untuk mengambil data dari tabel **employee** pada basis data **sql_port_1_music**. Mari kita bahas masing-masing bagian dari        query tersebut:

    1. **SELECT title, last_name, levels**: Ini adalah bagian SELECT dari query. Di sini, kita memilih tiga kolom dari tabel **employee**, yaitu **title**, **last_name**,          dan **levels**. Query ini akan mengambil data dari kolom-kolom ini untuk setiap baris yang memenuhi kondisi dari bagian berikutnya.

    2. **FROM sql_port_1_music.employee**: Ini adalah bagian FROM dari query. Di sini, kita menentukan dari tabel mana kita akan mengambil data, yaitu dari tabel                   **employee** yang berada dalam basis data **sql_port_1_music**.

    3. **ORDER BY levels DESC**: Ini adalah bagian ORDER BY dari query. Dengan menggunakan **ORDER BY**, kita dapat mengurutkan hasil berdasarkan kolom tertentu. Pada query        ini, kita mengurutkan data berdasarkan kolom **levels** secara menurun (descending), artinya nilai tertinggi akan berada di atas.

    4. **LIMIT 1**: Ini adalah bagian LIMIT dari query. Dengan menggunakan **LIMIT**, kita bisa membatasi jumlah baris yang akan ditampilkan. Pada query ini, kita hanya            ingin mengambil satu baris data, yaitu baris dengan nilai tertinggi dari kolom **levels** setelah diurutkan.

    Jadi, keseluruhan query ini akan mengambil data dari kolom **title**, **last_name**, dan **levels** dari tabel **employee** dalam basis data **sql_port_1_music**.           Kemudian, data akan diurutkan berdasarkan kolom **levels** dari nilai tertinggi ke nilai terendah (descending), dan hanya satu baris data dengan nilai tertinggi             tersebut yang akan ditampilkan sebagai hasil.

  - Hasil

2. Negara mana yang memiliki Faktur terbanyak?.
  - Query
  - Penjelasan Query
  - Hasil

3. Apa 3 nilai teratas dari total tagihan?.
  - Query
  - Penjelasan Query
  - Hasil

4. Kota mana yang memiliki pelanggan terbaik? Kami ingin mengadakan Festival Musik promosi di kota    tempat kami menghasilkan uang paling banyak. Tulis kueri yang mengembalikan satu kota yang         memiliki jumlah total faktur tertinggi. Kembalikan nama kota & jumlah semua total faktur.
  - Query
  - Penjelasan Query
  - Hasil

5. Siapa pelanggan terbaik? Pelanggan yang menghabiskan uang paling banyak akan dinyatakan sebagai    pelanggan terbaik. Tulis kueri yang mengembalikan orang yang menghabiskan uang paling banyak..
  - Query
  - Penjelasan Query
  - Hasil
    
## Pertanyaan Bagian 2

1. Tulis kueri untuk mengembalikan email, nama depan, nama belakang, & Genre semua pendengar Musik    Rock. Kembalikan daftar Anda yang diurutkan menurut abjad melalui email yang dimulai dengan A.
  - Query
  - Penjelasan Query
  - Hasil

2. Mari undang artis yang paling banyak menulis musik rock di dataset kita. Tulis kueri yang          mengembalikan nama Artis dan jumlah lagu total dari 10 band rock teratas.
  - Query
  - Penjelasan Query
  - Hasil

3. Kembalikan semua nama trek yang memiliki panjang lagu lebih panjang dari rata-rata panjang         lagu. Kembalikan Nama dan Milidetik untuk setiap trek. Diurutkan berdasarkan panjang lagu          dengan lagu terpanjang terdaftar terlebih dahulu..
  - Query
  - Penjelasan Query
  - Hasil


## Kontribusi

Kontribusi selalu sangat dihargai! Jika Anda ingin menambahkan contoh atau latihan baru, memperbaiki kesalahan, atau meningkatkan proyek ini secara keseluruhan, silakan ikuti langkah-langkah berikut:
1. Fork repositori ini.
2. Buat branch baru untuk fitur atau perbaikan Anda: `git checkout -b fitur-baru`.
3. Lakukan perubahan yang diinginkan.
4. Commit perubahan Anda: `git commit -m 'Menambahkan contoh query SQL baru'`.
5. Push ke branch Anda: `git push origin fitur-baru`.
6. Buat pull request ke branch `main` repositori ini.

Kami akan melihat kontribusi Anda dengan senang hati dan merespons secepat mungkin!
- SQL Client yang di pakai DBeaver untuk berinteraksi dengan database.

Terima kasih telah mengeksplorasi Proyek SQL Menarik ini! Semoga proyek ini membantu Anda meningkatkan pemahaman tentang SQL
© 2023 - Royjihan Maulana
