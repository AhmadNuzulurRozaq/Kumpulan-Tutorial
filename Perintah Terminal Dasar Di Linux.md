PERINTAH DASAR TERMINAL LINUX UBUNTU
------------------------------------

1. Menampilkan lokasi folder saat ini
   pwd (print working directory).

2. Menampilkan daftar file dan folder di direktori saat ini.
   ls | menampilkan isi folder dan file.
   ls -l | menampilkan folder dan isi file secara detail (izin, ukuran, tanggal)
   ls -a | menampilkan file tersembunyi (file yang diawali dengan titik).

3. Berpindah ke folder lain.
   cd (change directory).
   cd Documents | Masuk ke folder Documents.
   cd .. | Mundur 1 level ke folder sebelumnya.
   cd ~ | Kembali ke folder home user anda.

4. Membuat file baru.
   mkdir (make directory) | Membuat folder baru.
   contoh : mkdir Belajar

5. Membuat file baru.
   touch catatan.txt | Membuat file catatan.txt

6. Menyalin file atau folder.
   cp (copy).
   cp catatan.txt catatan2.txt | Menyalin file catatan.txt menjadi catatan2.txt
   cp -r folder_asal folder_tujuan | Menyalin folder beserta isinya ke folder tujuan.

7. Memindahkan dan mengganti nama file.
   mv catatan.txt /home/user/Documents | Memindahkan catatan.txt ke directori Documents.
   mv nama_lama.txt nama_baru.txt | Akan mengganti nama file dari yang lama ke yang baru.

8. Menghapus file dan folder
   rm (remove).
   rm catatan.txt | Menghapus file catatan.txt
   rm -r nama_folder | Menghapus folder beserta isinya.

9. Menampilkan seluruh isi file ke dalam terminal.
   cat catatan.txt | Maka isi teks di dalam catatan.txt akan ditampilkan di terminal.

10. Membuka teks editor sederhana di terminal
    nano catatan.txt | Maka akan membuka file catatan.txt dengan editor teks nano di terminal.

11.

