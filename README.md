Program sederhana input data karyawan menggunakan php

Membuat sebuah porgram sederhana yaitu input data karyawan menggunakan bahasa pemrogramman PHP

Tools yang dibutuhkan.

- XAMPP
- Visual Studio Code
- Browser (google chrome)

Pertama buat lah folder di dalam htdocs dengan nama Lab2Web lalu buat file bernama index.php untuk penamaan folder dan file kalian bebas menamakannya. Setelah itu buka folder tersebut dengan Visual Studio Code seperti gambar dibawah ini

![image](https://github.com/raudahmusrifa/Lab2Web/assets/115474431/57316af0-9913-4eb4-8529-c11cb6ba6567)

selanjutnya buka file index.php lalu ikuti kode seperti gambar dibawah :

![image](https://github.com/raudahmusrifa/Lab2Web/assets/115474431/c86acd46-ef94-4893-999c-0694453ef7df)

Pembahasan Pada kode diatas merupakan kode php dalam menangani formulir yang akan diinput,

if (isset($_POST['submit'])) { ini pengecekan jika ada post submit yang dikirim maka lakukan perintah berikut, jika tidak ada dia keluar blok kurang kurawal buka / tutup

Pada bagian berikut dilakukan pengecekan mengenai pekerjaan, jika pekerjaannya sebagai Software Engineer maka gaji nya 23000000 dan seterusnya tergantung pada yang diinputkan nanti didalam formulir

    $pekerjaan = $_POST["pekerjaan"];
      if ($pekerjaan == "Software Engineer") {
        $gaji = 23000000;
      } else if ($pekerjaan == "Data Analyst") {
        $gaji = 25000000;
      } else if ($pekerjaan == "Design Graphic") {
        $gaji = 19000000;
      } else if ($pekerjaan == "Network Engineer") {
        $gaji = 22000000;
      } else if ($pekerjaan == "QA Engineer") {
        $gaji = 18000000;
      } else if ($pekerjaan == "DevOps Engineer") {
        $gaji = 23500000;
      } else {
        $gaji = 0;
      }

Selanjutnya pada bagian blok kode berikut merupakan perhitungan umur berdasarkan tanggal lahir yang diinputkan, kita menggunakan fungsi bawaan php yaitu DateTime() yang mana nanti kita dapat mengetahui umur yang akan diinputkan berdasarkan tanggal lahirnya. lalu kita simpan di variabel umur.

    $tanggal_lahir = new DateTime($_POST['tanggal_lahir']);
    
      $hari_ini = new DateTime('today');
      $tahun = $tanggal_lahir->diff($hari_ini)->y;
      $bulan = $tanggal_lahir->diff($hari_ini)->m;
      $hari = $tanggal_lahir->diff($hari_ini)->d;
    
      $umur = $tahun . " tahun " . $bulan . " bulan " . $hari . " hari ";

lanjut ke kode berikut :

kode berikut merupakan kerangka html yang akan menampilkan formulir dan data yang diinputkan, pada kode ini kita menambahkan style css agar terlihat menarik.

![image](https://github.com/raudahmusrifa/Lab2Web/assets/115474431/f427995a-eebb-4c0d-8d86-17d0304462b5)


![image](https://github.com/raudahmusrifa/Lab2Web/assets/115474431/d1961311-3cef-4cc6-89ce-7092476b3f1f)

Selanjutnya tambahkan kode berikut :

pada kode dibawah ini merupakan tag formulir html. sebagai formulir dan hasil dari inputan yang akan diinputkan nanti.


![image](https://github.com/raudahmusrifa/Lab2Web/assets/115474431/fa53018d-000d-4906-a9d5-d9af2bbe109e)

setelah selesai saatnya kita jalankan programnya dengan cara buka xampp control panel lalu start apache, jika sudah buka browser lalu ketikan localhost/Lab2Web

Berikut hasil program yang akan muncul sebelum diinput dan sesudah diinput :


![image](https://github.com/raudahmusrifa/Lab2Web/assets/115474431/e9a136c3-f1b2-4281-99c8-0509f18e4339)


![image](https://github.com/raudahmusrifa/Lab2Web/assets/115474431/0f8b6321-2b2c-4199-bd2e-e9c5dec7d2ab)

Selesai, Terima kasih.








