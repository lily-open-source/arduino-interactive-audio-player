## Secara Simple

### Detail Kode

1. **Kompatibilitas Mikrokontroler**: ????.
2. **Koneksi LCD**: Menggunakan layar I2C LCD 2004.
3. **Indikator**: Dilengkapi dengan satu atau lebih LED untuk indikasi status.
4. **Keypad**: Memiliki keypad 10 (0-9) tombol ditambah 2 tombol tambahan.
5. **Umpan Balik Audio**: Termasuk buzzer untuk peringatan suara.
6. **Penyimpanan**: Terhubung ke modul kartu memori.
7. **Output Audio**: Terhubung ke modul speaker melalui I2S.

### Penggunaan

1. **Menu Sambutan**:
    - Perangkat menyambut pengguna dan meminta mereka untuk memilih tindakan:
        a. Mendengarkan
        b. Menjawab

2. **Mode Mendengarkan**:
    - Pemilihan dilakukan menggunakan 2 tombol khusus.
    - Konfirmasi prompt: "Apakah Anda yakin?" (Pilihan: Ya/Tidak).
    - Jika dikonfirmasi, pengguna diminta memasukkan nomor file menggunakan keypad 10 tombol.
    - Konfirmasi diperlukan sebelum memutar suara.
    - Gunakan tombol khusus untuk tindakan seperti hapus/masuk.
    - Fungsi Batal/Kembali memungkinkan pengguna untuk kembali ke langkah sebelumnya.

3. **Mode Menjawab**:
    - File acak diputar, dan pengguna diminta menebak nomor file.
    - Tebakan benar: +1 skor.
    - Tebakan salah: -1 skor.
    - Permainan berakhir saat skor mencapai 0 (Game Over) atau 10 (Kemenangan).
    - Pilihan keluar atau lanjutkan tersedia menggunakan 2 tombol khusus. Skor awal ditetapkan pada 5.

## Secara Detail

### Detail Kode

#### Komponen Hardware

1. **Mikrokontroler**:
   - Masih didiskusikan.

2. **Layar**:
   - LCD I2C 2004 (20 karakter x 4 baris).

3. **Indikator**:
   - Satu atau lebih LED untuk menunjukkan status yang berbeda (misalnya, daya nyala, mode operasi).

4. **Keypad**:
   - Keypad numerik 10 tombol untuk input pengguna (tombol diberi label 0-9).
   - Dua tombol tambahan untuk navigasi (diberi label Enter dan Delete).

5. **Umpan Balik Audio**:
   - Buzzer untuk memberikan peringatan suara.

6. **Penyimpanan**:
   - Modul kartu memori untuk menyimpan file audio.

7. **Output Audio**:
   - Modul speaker yang terhubung melalui I2S untuk memutar suara.

#### Persyaratan Fungsional

##### Menu Sambutan

1. **Prompt Awal**:
   - Saat dinyalakan, perangkat menampilkan pesan selamat datang di LCD dan meminta pengguna untuk memilih tindakan:
     - a. Mendengarkan
     - b. Menjawab

2. **Proses Pemilihan**:
   - Pengguna memilih opsi menggunakan dua tombol khusus (Enter dan Delete).

##### Mode Mendengarkan

1. **Konfirmasi**:
   - Setelah memilih "Mendengarkan", perangkat meminta konfirmasi: "Anda yakin? (Ya/Tidak)".
   - Pengguna mengonfirmasi menggunakan tombol khusus.

2. **Pemilihan File**:
   - Setelah konfirmasi, perangkat meminta pengguna untuk memasukkan nomor file menggunakan keypad 10 tombol.
   - Pengguna dapat memasukkan nomor dan mengonfirmasi dengan tombol Enter.

3. **Memutar Audio**:
   - Perangkat meminta konfirmasi lagi sebelum memutar suara: "Putar file X? (Ya/Tidak)".
   - Jika dikonfirmasi, file suara yang sesuai dengan nomor yang dimasukkan akan diputar melalui speaker.

4. **Navigasi**:
   - Pengguna dapat membatalkan dan kembali ke langkah sebelumnya kapan saja menggunakan tombol Delete.

##### Mode Menjawab

1. **Mulai Permainan**:
   - Perangkat secara acak memilih dan memutar file audio.
   - Pengguna diminta untuk menebak nomor file dengan memasukkannya menggunakan keypad 10 tombol.

2. **Penilaian**:
   - Jika tebakan benar, skor pengguna bertambah 1.
   - Jika tebakan salah, skor pengguna berkurang 1.
   - Skor awal diatur ke 5.

3. **Kondisi Akhir**:
   - Permainan berakhir jika skor pengguna mencapai 0 (Game Over) atau 10 (Victory).
   - Perangkat memberikan opsi untuk keluar atau melanjutkan permainan menggunakan tombol khusus.

4. **Navigasi**:
   - Pengguna dapat keluar dari permainan kapan saja menggunakan dua tombol khusus (Exit/Lanjutkan).

#### Alur Interaksi Pengguna

1. **Mulai**:
   - Tampilan: "Selamat datang! Apa yang ingin Anda lakukan?"
   - Opsi: "a. Mendengarkan b. Menjawab"

2. **Mode Mendengarkan**:
   - Tampilan: "Anda yakin? (Ya/Tidak)"
   - Jika Ya: "Masukkan nomor file:"
   - Setelah memasukkan: "Putar file X? (Ya/Tidak)"
   - Jika Ya: Putar file suara.
   - Gunakan Delete untuk membatalkan dan kembali ke langkah sebelumnya.

3. **Mode Menjawab**:
   - Putar file audio acak.
   - Tampilan: "Tebak nomor file:"
   - Setelah menebak: "Benar!" atau "Salah!"
   - Perbarui skor: "Skor: X"
   - Kondisi akhir permainan: "Game Over" atau "Victory!"
   - Opsi untuk keluar atau melanjutkan.

### Pertimbangan Tambahan

- **Penanganan Kesalahan**:
  - Tampilkan pesan kesalahan yang sesuai untuk input tidak valid atau file tidak ditemukan.

- **Manajemen Daya**:
  - Pastikan penggunaan daya yang efisien untuk memperpanjang masa pakai baterai jika perangkat portabel.

- **Umpan Balik Pengguna**:
  - Gunakan LED dan buzzer untuk memberikan umpan balik tambahan untuk tindakan pengguna (misalnya, input diterima, kesalahan).

- **Manajemen Memori**:
  - Kelola penyimpanan dan pengambilan kartu memori dengan efisien untuk menangani beberapa file audio.
