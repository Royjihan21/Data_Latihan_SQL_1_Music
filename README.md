# Proyek SQL Music

Selamat datang di Proyek SQL Menarik! Proyek ini dirancang untuk memberikan pengalaman belajar yang menarik tentang SQL dan penggunaannya dalam manajemen database.

## Daftar Isi

- [Schema Diagram](#schema-diagram)
- [Pertanyaan Bagian 1](#pertanyaan-bagian-1)
- [Pertanyaan Bagian 2](#pertanyaan-bagian-2)
- [Kontribusi](#kontribusi)

## Schema Diagram

<div align="center">
  <img src="https://github.com/Royjihan21/Data_Latihan_SQL_1_Music/blob/main/schema_diagram.png">
</div>

## Pertanyaan Bagian 1

### 1. Siapa karyawan paling senior berdasarkan jabatan.
  - **Query**
    ***
      select title,last_name,levels 
      from sql_port_1_music.employee 
      order by levels desc 
      limit 1;

  - **Penjelasan Query**
    ***
    Query di atas adalah sebuah perintah SQL untuk mengambil data dari tabel **employee** pada basis data **sql_port_1_music**. Mari kita bahas masing-masing bagian dari       query tersebut:

    1. **SELECT title, last_name, levels**: Ini adalah bagian SELECT dari query. Di sini, kita memilih tiga kolom dari tabel **employee**, yaitu **title**, **last_name**,          dan **levels**. Query ini akan mengambil data dari kolom-kolom ini untuk setiap baris yang memenuhi kondisi dari bagian berikutnya.

    2. **FROM sql_port_1_music.employee**: Ini adalah bagian FROM dari query. Di sini, kita menentukan dari tabel mana kita akan mengambil data, yaitu dari tabel                   **employee** yang berada dalam basis data **sql_port_1_music**.

    3. **ORDER BY levels DESC**: Ini adalah bagian ORDER BY dari query. Dengan menggunakan **ORDER BY**, kita dapat mengurutkan hasil berdasarkan kolom tertentu. Pada              query ini, kita mengurutkan data berdasarkan kolom **levels** secara menurun (descending), artinya nilai tertinggi akan berada di atas.

    4. **LIMIT 1**: Ini adalah bagian LIMIT dari query. Dengan menggunakan **LIMIT**, kita bisa membatasi jumlah baris yang akan ditampilkan. Pada query ini, kita hanya            ingin mengambil satu baris data, yaitu baris dengan nilai tertinggi dari kolom **levels** setelah diurutkan.

    Jadi, keseluruhan query ini akan mengambil data dari kolom **title**, **last_name**, dan **levels** dari tabel **employee** dalam basis data **sql_port_1_music**.          Kemudian, data akan diurutkan berdasarkan kolom **levels** dari nilai tertinggi ke nilai terendah (descending), dan hanya satu baris data dengan nilai tertinggi            tersebut yang akan ditampilkan sebagai hasil.

  - **Hasil**
    <div align="center">
    <img src="https://github.com/Royjihan21/Data_Gambar_SQL/blob/main/Picture_Porto_1_SQL_Music/Bagian_1_Q1.png">
    </div>

### 2. Negara mana yang memiliki Faktur terbanyak?.
  - **Query**
    ***
    select count(*)as c,billing_country 
    from sql_port_1_music.invoice
    group by billing_country 
    order by c desc;

  - **Penjelasan Query**
    ***
    Query di atas adalah perintah SQL yang dirancang untuk mengambil jumlah total faktur (**invoice**) untuk setiap negara (**billing_country**) dari tabel **invoice**         dalam database **sql_port_1_music**. Mari kita bahas masing-masing bagian dari query tersebut:

    1. **SELECT COUNT(*) AS c, billing_country**: Bagian ini dari query menghitung jumlah total baris untuk setiap negara dalam kolom **billing_country**. **COUNT(*)**            adalah fungsi agregat yang menghitung jumlah baris dalam sebuah set data. **AS c** digunakan untuk memberi nama alias **c** untuk hasil dari **COUNT(*)**.

    2. **FROM sql_port_1_music.invoice**: Bagian ini menentukan tabel sumber data, yaitu tabel **invoice** dalam database **sql_port_1_music**.

    3. **GROUP BY billing_country**: Bagian ini mengelompokkan hasil berdasarkan negara (**billing_country**). Artinya, untuk setiap negara yang unik dalam kolom                  **billing_country**, fungsi **COUNT(*)** akan dijalankan dan menghasilkan satu baris dalam hasil akhir.

    4. **ORDER BY c DESC**: Bagian ini mengurutkan hasil berdasarkan jumlah faktur yang dihitung (**c**) dalam urutan menurun (**DESC**). Artinya, negara dengan jumlah            faktur terbanyak akan muncul di atas hasil.

    Jadi, keseluruhan query ini akan menghitung jumlah total faktur untuk setiap negara, mengelompokkan hasil berdasarkan negara, dan mengurutkan hasil dari jumlah faktur      terbanyak ke terendah.

  - **Hasil**
    <div align="center">
    <img src="https://github.com/Royjihan21/Data_Gambar_SQL/blob/main/Picture_Porto_1_SQL_Music/Bagian_1_Q2.png">
    </div>
### 3. Apa 3 nilai teratas dari total tagihan?.
  - **Query**
    ***
    select total 
    from sql_port_1_music.invoice 
    order by total desc;

  - **Penjelasan Query**
    ***
    Query di atas adalah perintah SQL untuk mengambil data dari tabel **invoice** dalam database **sql_port_1_music** dan mengurutkannya berdasarkan kolom **total** secara     menurun (descending). Mari kita bahas masing-masing bagian dari query tersebut:

    1. **SELECT total**: Ini adalah bagian SELECT dari query. Di sini, kita memilih kolom **total** dari tabel **invoice**. Query ini akan mengambil data dari kolom               **total** untuk setiap baris dalam tabel **invoice**.

    2. **FROM sql_port_1_music.invoice**: Ini adalah bagian FROM dari query. Di sini, kita menentukan dari tabel mana kita akan mengambil data, yaitu tabel **invoice**            dalam database **sql_port_1_music**.

    3. **ORDER BY total desc**: Ini adalah bagian ORDER BY dari query. Dengan menggunakan **ORDER BY**, kita dapat mengurutkan hasil berdasarkan kolom tertentu. Pada query        ini, kita mengurutkan data berdasarkan kolom **total** secara menurun (descending), artinya nilai tertinggi akan berada di atas.

    Jadi, keseluruhan query ini akan mengambil data dari kolom **total** dalam tabel **invoice** dan mengurutkannya dari nilai tertinggi ke nilai terendah berdasarkan          kolom **total**. Hasilnya akan berupa data yang diurutkan berdasarkan kolom **total** dalam urutan menurun.
    
  - **Hasil**
    <div align="center">
    <img src="https://github.com/Royjihan21/Data_Gambar_SQL/blob/main/Picture_Porto_1_SQL_Music/Bagian_1_Q3.png">
    </div>

### 4. Kota mana yang memiliki pelanggan terbaik? Kami ingin mengadakan Festival Musik promosi di kota    tempat kami menghasilkan uang paling banyak. Tulis kueri yang mengembalikan satu kota yang memiliki jumlah total faktur tertinggi. Kembalikan nama kota & jumlah semua total faktur.
  - **Query**
    ***
    select billing_city,sum(total) as invoiceTotal 
    from sql_port_1_music.invoice 
    group by billing_city 
    order by invoiceTotal desc 
    limit 1;

  - **Penjelasan Query**
    ***
    Query di atas adalah perintah SQL yang digunakan untuk menghitung total nilai faktur (**total**) untuk setiap kota (**billing_city**) dari tabel **invoice** dalam          database **sql_port_1_music**, kemudian mengelompokkan hasil berdasarkan kota, mengurutkan hasil berdasarkan total nilai faktur dari yang tertinggi ke terendah             (descending), dan membatasi hasilnya hanya untuk satu baris teratas (dengan nilai faktur tertinggi).

    Mari kita bahas masing-masing bagian dari query tersebut:

    1. **SELECT billing_city, SUM(total) AS invoiceTotal**: Bagian ini dari query memilih dua kolom, yaitu **billing_city** dan total jumlah (**SUM(total)**) nilai faktur.        **SUM(total)** adalah fungsi agregat yang digunakan untuk menghitung total nilai dari kolom **total** untuk setiap kota (**billing_city**), dan **AS invoiceTotal**         digunakan untuk memberi nama alias **invoiceTotal** untuk hasil dari total jumlah.

    2. **FROM sql_port_1_music.invoice**: Bagian ini menentukan tabel sumber data, yaitu tabel **invoice** dalam database **sql_port_1_music**.

    3. **GROUP BY billing_city**: Bagian ini mengelompokkan hasil berdasarkan kota (**billing_city**). Artinya, fungsi **SUM(total)** akan dijalankan untuk setiap kota            yang unik dalam kolom **billing_city**, dan menghasilkan satu baris dalam hasil akhir untuk setiap kota.

    4. **ORDER BY invoiceTotal DESC**: Bagian ini mengurutkan hasil berdasarkan total jumlah nilai faktur (**invoiceTotal**) dari yang tertinggi ke terendah (descending).         Hal ini dilakukan karena kita ingin melihat kota dengan total nilai faktur tertinggi berada di bagian atas hasil.

    5. **LIMIT 1**: Bagian ini membatasi hasil hanya untuk satu baris teratas saja (dengan total nilai faktur tertinggi). Sehingga, hasil yang dihasilkan hanya akan               menampilkan satu baris data, yaitu kota dengan total nilai faktur tertinggi.

       Jadi, keseluruhan query ini akan menghitung total nilai faktur untuk setiap kota, mengelompokkan hasil berdasarkan kota, mengurutkan hasil dari nilai total                 tertinggi ke terendah, dan hanya menampilkan satu baris data, yaitu kota dengan total nilai faktur tertinggi.

  - **Hasil**
    <div align="center">
    <img src="https://github.com/Royjihan21/Data_Gambar_SQL/blob/main/Picture_Porto_1_SQL_Music/Bagian_1_Q4.png">
    </div

### 5. Siapa pelanggan terbaik? Pelanggan yang menghabiskan uang paling banyak akan dinyatakan sebagai    pelanggan terbaik. Tulis kueri yang mengembalikan orang yang menghabiskan uang paling banyak..
  - **Query**
    ***
    SELECT 
    customer.customer_id,
    first_name,
    last_name,
    SUM(total) AS total_spending
    FROM 
    sql_port_1_music.customer
    JOIN 
    sql_port_1_music.invoice ON customer.customer_id = invoice.customer_id 
    GROUP BY 
    customer.customer_id, first_name, last_name
    ORDER BY 
    SUM(total) DESC
    LIMIT 1;

  - **Penjelasan Query**
    ***
    Query di atas adalah perintah SQL yang digunakan untuk menemukan pelanggan (**customer**) dengan total pengeluaran (**total**) tertinggi dari database                      **sql_port_1_music**. Untuk melakukan ini, query ini menggunakan JOIN untuk menggabungkan data dari tabel **customer** dan tabel **invoice**. 

    Berikut penjelasan lebih detail untuk masing-masing bagian dari query tersebut:

    1. **SELECT customer.customer_id, first_name, last_name, SUM(total) AS total_spending**: Bagian ini dari query memilih empat kolom, yaitu **customer_id**,                     **first_name**, **last_name**, dan total jumlah (**SUM(total)**) nilai faktur. **SUM(total)** adalah fungsi agregat yang digunakan untuk menghitung total nilai dari        kolom **total** untuk setiap pelanggan (**customer_id**), dan **AS total_spending** digunakan untuk memberi nama alias **total_spending** untuk hasil dari total            jumlah.

    2. **FROM sql_port_1_music.customer**: Bagian ini menentukan tabel sumber data utama, yaitu tabel **customer** dalam database **sql_port_1_music**.

    3. **JOIN sql_port_1_music.invoice ON customer.customer_id = invoice.customer_id**: Bagian ini menggabungkan data dari tabel **invoice** dengan tabel **customer**             berdasarkan kondisi yang ditentukan, yaitu di mana **customer_id** di tabel **customer** sama dengan **customer_id** di tabel **invoice**. 

    4. **GROUP BY customer.customer_id, first_name, last_name**: Bagian ini mengelompokkan hasil berdasarkan **customer_id**, **first_name**, dan **last_name**. Artinya,          fungsi **SUM(total)** akan dijalankan untuk setiap pelanggan yang unik (dikenali berdasarkan **customer_id**, **first_name**, dan **last_name**), dan menghasilkan          satu baris dalam hasil akhir untuk setiap pelanggan.

    5. **ORDER BY SUM(total) DESC**: Bagian ini mengurutkan hasil berdasarkan total jumlah nilai faktur (**SUM(total)**) dari yang tertinggi ke terendah (descending). Hal         ini dilakukan karena kita ingin melihat pelanggan dengan total nilai faktur tertinggi berada di bagian atas hasil.

    6. **LIMIT 1**: Bagian ini membatasi hasil hanya untuk satu baris teratas saja (dengan total nilai faktur tertinggi). Sehingga, hasil yang dihasilkan hanya akan               menampilkan satu baris data, yaitu pelanggan dengan total nilai faktur tertinggi.

       Jadi, keseluruhan query ini akan menghitung total nilai faktur untuk setiap pelanggan, mengelompokkan hasil berdasarkan **customer_id**, **first_name**, dan                **last_name**, mengurutkan hasil dari nilai total tertinggi ke terendah, dan hanya menampilkan satu baris data, yaitu pelanggan dengan total nilai faktur tertinggi.

  - **Hasil**
    <div align="center">
    <img src="https://github.com/Royjihan21/Data_Gambar_SQL/blob/main/Picture_Porto_1_SQL_Music/Bagian_1_Q5.png">
    </div
    
## Pertanyaan Bagian 2

### 1. Tulis kueri untuk mengembalikan email, nama depan, nama belakang, & Genre semua pendengar Musik    Rock. Kembalikan daftar Anda yang diurutkan menurut abjad melalui email yang dimulai dengan A.
  - **Query**
    ***
  - **Penjelasan Query**
    ***
  - **Hasil**

### 2. Mari undang artis yang paling banyak menulis musik rock di dataset kita. Tulis kueri yang          mengembalikan nama Artis dan jumlah lagu total dari 10 band rock teratas.
  - **Query**
    ***
  - **Penjelasan Query**
    ***
  - **Hasil**

### 3. Kembalikan semua nama trek yang memiliki panjang lagu lebih panjang dari rata-rata panjang         lagu. Kembalikan Nama dan Milidetik untuk setiap trek. Diurutkan berdasarkan panjang lagu          dengan lagu terpanjang terdaftar terlebih dahulu..
  - **Query**
    ***
  - **Penjelasan Query**
    ***
  - **Hasil**


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
