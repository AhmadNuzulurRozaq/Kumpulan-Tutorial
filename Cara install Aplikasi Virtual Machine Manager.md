===========================================================
CARA INSTALL VIRTUAL MACHINE MANAGER DI UBUNTU 24.04 LTS
===========================================================
- by : Ahmad Nuzulur Rozaq
===========================================================

01. Update repositori
    Perintah : sudo apt update

02. Setelah terupdate, cek apakah laptop mendukung virtualisasi
    Perintah : egrep -c '(vmx|svm)' /proc/cpuinfo
    Output   : 4

    Fungsi perintah diatas :
    -> egrep         : Mencari teks tertentu di dalam file.
    -> -c            : Count (menghitung) berapa kali teks tersebut ditemukan.
    -> '(vmx|svm)'   : Kode fitur virtualisasi (vmx untuk Intel, svm untuk AMD).
    -> /proc/cpuinfo : File sistem yang berisi detail tentang CPU kamu.

    Catatan  : Jika outputnya lebih dari 0 (misalnya 4, 8, 12, dst) Berarti laptop/PC support. 
               Jika 0, maka harus diaktifkan dulu di pengaturan BIOS.

03. Install aplikasi pendukung nya
    Perintah : sudo apt install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils virt-manager
    
    Fungsi perintah diatas :
    -> sudo                  : Memberikan akses root.
    -> apt                   : Menjalankan Package Manajer.
    -> install               : install: Perintah untuk memasang aplikasi.
    -> qemu-kvm              : Software utama yang melakukan emulasi perangkat keras.
    -> libvirt-daemon-system : Layanan sistem (background service) yang menjalankan virtualisasi.
    -> libvirt-clients       : Alat untuk berinteraksi dengan layanan virtualisasi.
    -> bridge-utils          : Alat jaringan agar Virtual Machine (VM) kamu bisa terhubung ke internet seolah-olah dia adalah perangkat fisik yang terpisah (Bridge network).
    -> virt-manager          : Antarmuka grafis (GUI) agar kamu bisa mengelola VM dengan mudah (seperti VirtualBox), tanpa harus mengetik perintah rumit terus-menerus.

04. Aktifkan layanan virtualisasi
    Perintah : sudo systemctl enable --now libvirtd
    
    Fungsi perintah diatas :
    -> sudo      : Memberikan akses root.
    -> systemctl : Alat kontrol untuk sistem(systemd).
    -> enable    : Mengatur agar layanan ini otomatis menyala setiap kali komputer dinyalakan (booting).
    -> --now     : Menyalakan layanan tersebut sekarang juga tanpa perlu restart komputer.
    -> libvirtd  : Nama layanan daemon untuk libvirt.

05. Cek status layanan libvirtd jalan/tidak
    Perintah : sudo systemctl status libvirtd

    Fungsi perintah diatas : 
    -> sudo      : Memberikan akses root.
    -> systemctl : Alat kontrol untuk sistem(systemd).
    -> status    : Cek keadaan layanan.
    -> libvirtd  : Nama layanan daemon untuk libvirt.

06. Tambahkan virtual ke akun utama
    Perintah : sudo usermod -aG libvirt,kvm $USER

    Fungsi perintah diatas :
    -> sudo        : Memberikan akses root.
    -> usermod     : Perintah untuk memodifikasi akun user.
    -> -aG         : Append Group (tambahkan ke grup).
    -> libvirt,kvm : kvm & libvirt: Nama grup yang memiliki izin akses ke mesin virtual.
    -> $USER       : $USER: Variabel yang otomatis terisi dengan nama user kamu saat ini (jadi kamu tidak perlu mengetik nama usermu secara manual).

    CATATAN : Wajib logout / restart setelah menerapkan perubahan diatas.