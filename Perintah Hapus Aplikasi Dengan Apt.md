=======================================================
FUNGSI APT REMOVE, APT PURGE, APT CLEAN, APT AUTOREMOVE
=======================================================
- by : Ahmad Nuzulur Rozaq
=======================================================

01. APT REMOVE

    Perintah : sudo apt remove [nama_aplikasi]
	Fungsi   : Menghapus sistem inti aplikasi nya / aplikasi utama tanpa menghapus konfigurasinya.

02. APT PURGE

    Perintah : sudo apt purge [nama_aplikasi]
	Fungsi   : Menghapus sistem inti aplikasi nya / aplikasi utama sekaligus file konfigurasinya.

03. APT CLEAN

	Perintah : sudo apt clean
	Fungsi   : Membersihkan cache installer hasil download aplikasi melalui apt install.

04. APT AUTOREMOVE

	Perintah : sudo apt autoremove
	Fungsi   : Membersihkan file depedensi / library aplikasi yang sudah tidak dibutuhkan lagi.

Dibawah ini merupakan perintah kombinasi untuk menghapus aplikasi + konfigurasinya + depedensi / library nya.
Perintah : sudo apt purge --autoremove [nama_aplikasi]
