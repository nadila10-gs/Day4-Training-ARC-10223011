# Day4-Training-ARC-10223011
Berikut adalah konfigurasi dasar untuk router agar mendukung IPv6 dan menghubungkan jaringan:
enable
configure terminal
ipv6 unicast-routing

interface g0/0
 ipv6 address 2001:DB8:ACAD:100::1/64
 ipv6 enable
 no shutdown
exit

interface g0/1
 ipv6 address 2001:DB8:ACAD:200::1/64
 ipv6 enable
 no shutdown
exit

exit

Pastikan PC memiliki konfigurasi berikut:
IPv6 Address: 2001:DB8:ACAD:100::50/64
Gateway: 2001:DB8:ACAD:100::1

uji koneksi dengan perintah berikut:
ping 2001:DB8:ACAD:100::1  # Tes koneksi ke router
ping 2001:DB8:ACAD:200::1  # Tes koneksi ke jaringan lain

Jalankan perintah konfigurasi di atas pada CLI perangkat.

Lakukan uji koneksi menggunakan ping
