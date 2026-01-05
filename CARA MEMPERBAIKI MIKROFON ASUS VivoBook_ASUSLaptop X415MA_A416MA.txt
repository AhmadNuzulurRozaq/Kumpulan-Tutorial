CARA MEMPERBAIKI MIKROFON INTERNAL ASUS VivoBook_ASUSLaptop X415MA_A416MA
--------------------------------------------------------------------------

1. Buka Terminal Ubuntu
2. Ketik : sudo nano /etc/modprobe.d/alsa-base.conf
3. Setelah terbuka geser paling bawah dan tambahkan baris
   --> options snd-hda-intel model=alc255-asus
4. Tekan CTRL + O lalu enter, kemudian tekan CTRL + X untuk keluar
5. Restart laptop nya.
