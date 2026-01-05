PERINTAH GIT UNTUK UPLOAD FILE PROJEK KE GITHUB
-----------------------------------------------

1. git init
   Fungsi : Supaya folder projek kita di deteksi oleh git dan di lacak.

2. git status
   Fungsi : Untuk melihat file mana yang belum tersimpan atau baru diubah.
   Catatan : Jika ada file yang berwarna merah itu artinya belum masuk ke antrean untuk disimpan.

3. git add .
   Fungsi : Memilih folder dan file mana saja sebelum di upload.
   Penjelasan : tanda (.) berarti memilih semua folder dan file.

4. git commit -m "ISI PESAN / KETERANGAN"
   Fungsi : Simpan perubahan
   Penjelasan : (-m) singkatan dari message. Memberi label/pesan apa yang baru saja ditambahkan.

5. git branch -M main
   Fungsi : Mengubah cabang ke main.

6. git remote add origin https://github.com/USERNAME/NAMA-REPO.git
   Fungsi : Menghubungkan ke Github melalui remote.

7. git push -u origin main
   Fungsi : Mengupload dan mengurim seluruh file ke Github.
   Penjelasan : - push = Dorong/Upload data.
                - -u = Upstream.
                - origin main = kirim ke alamat origin di cabang main.
8. git push
   Fungsi : Jika projek sudah pernah diedit oleh orang lain, maka perintah tersebut akan mengupdate data terbaru.
