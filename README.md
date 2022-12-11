# Jarkom-Modul-5-B08-2022

## Anggota Kelompok
<table>
 	<tr>
 		<td> Nama </td>
 		<td> NRP</td>
 	</tr>
 	<tr>
 		<td> Aaliyah Farah Adibah </td>
 		<td> 5025201070 </td>
 	</tr>
  <tr>
 		<td> Rafael Asi Kristanto Tambunan </td>
 		<td> 5025201168 </td>
 	</tr>
  <tr>
 		<td> Sejati Bakti Raga </td>
 		<td> 5025201007 </td>
 	</tr>
 </table>
 
 ## Daftar Isi
  + [Soal A](#soal-a)
  + [Soal B](#soal-b)
  + [Soal C](#soal-c)
  + [Soal D](#soal-d)
  + [Soal D1](#soal-1)
  + [Soal D2](#soal-2)
  + [Soal D3](#soal-3)
  + [Soal D4](#soal-4)
  + [Soal D5](#soal-5)
  + [Soal D6](#soal-6)
  + [Kendala](#kendala)
  
  ## Soal A
 
   ***Tugas pertama kalian yaitu membuat topologi jaringan sesuai dengan rancangan yang diberikan Loid dibawah ini. Keterangan :***
   
   - Eden adalah DNS Server 
   - WISE adalah DHCP Server
   - Garden dan SSS adalah Web Server
   - Jumlah Host pada Forger adalah 62 host
   - Jumlah Host pada Desmond adalah 700 host
   - Jumlah Host pada Blackbell adalah 255 host
   - Jumlah Host pada Briar adalah 200 host
  
  ![topologi ](https://user-images.githubusercontent.com/73101444/206859823-eb098747-0457-4928-bf36-cc242de7ce07.png)
 
  
  ## Soal B
  
  ***Untuk menjaga perdamaian dunia, Loid ingin meminta kalian untuk membuat topologi tersebut menggunakan teknik CIDR atau VLSM setelah melakukan subnetting.***
  
  ### Tree:
  
  ![praktikum5 drawio](https://user-images.githubusercontent.com/73101444/206859885-679f1f02-7bb3-4be8-a21c-2c457239f0de.png)

  ### Pembagian IP:
  | Subnet  | Jumlah IP | Netmask | subnetmask | nid |
  | :---         |     :---:      |          ---: | :---:      | :---:      |
  | ------------- | ------------- | ------------- | ------------- | ------------- |
  | A1 | 2 | /30 | 255.255.255.252 | 10.7.0.0/30 |
  | A2 | 2 | /30 | 255.255.255.252 | 10.7.0.4/30 |
  | A3 | 201 | /24 | 255.255.255.0 | 10.7.2.0/24 |
  | A4 | 256 | /24 | 255.255.255.0 | 10.7.3.0/24 |
  | A5 | 63 | /26 | 255.255.255.192 | 10.7.0.64/26 |
  | A6 | 701 | /22 | 255.255.252.0 | 10.7.4.0/22 |
  | A7 | 4 | /29 | 255.255.255.248 | 10.7.0.16/29 |
  | A8 | 4 | /29 | 255.255.255.248 | 10.7.0.24/29 |
  | Jumlah | 1233 | /21 | 255.255.248.0 | - |
  
  
 ### SETTING INTERFACE PADA GNS3
 **Strix**
```
auto eth0
iface eth0 inet dhcp
auto eth1
iface eth1 inet static
        address 192.186.0.1
        netmask 255.255.255.252
auto eth2
iface eth2 inet static
         address 192.186.0.5
         netmask 255.255.255.252
```

**Ostania**

```
auto eth0
iface eth0 inet static
          address 10.7.0.6
          netmask 255.255.255.252
          gateway 10.7.0.5

auto eth1
iface eth1 inet static
          address 10.7.3.1
          netmask 255.255.255.0

auto eth2
iface eth2 inet static
          address 10.7.2.1
          netmask 255.255.255.0

auto eth3
iface eth3 inet static
          address 10.7.0.25
          netmask 255.255.255.248
```


**Westalis**

```
auto eth0
iface eth0 inet static
        address 10.7.0.2
        netmask 255.255.255.252
        gateway 10.7.0.1

auto eth1
iface eth1 inet static
        address 10.7.0.17
        netmask 255.255.255.248

auto eth2
iface eth2 inet static
         address 10.7.0.65
         netmask 255.255.255.192

auto eth3
iface eth3 inet static
         address 10.7.4.1
         netmask 255.255.252.0
```

**Eden**

```
auto eth0
iface eth0 inet static
       address 10.7.0.18
       netmask 255.255.255.248
       gateway 10.7.0.17
```

**WISE**

```
auto eth0
iface eth0 inet static
       address 10.7.0.19
       netmask 255.255.255.248
       gateway 10.7.0.17
```

**Forger(62Host)**

```
auto eth0
iface eth0 inet static
      address 10.7.0.66
      netmask 255.255.255.192
      gateway 10.7.0.65
```

**Desmond(700Host)**

```
auto eth0
iface eth0 inet static
       address 10.7.4.2
      netmask 255.255.252.0
       gateway 10.7.4.1
```

**Briar(200Host)**

```
auto eth0
iface eth0 inet static
       address 10.7.2.2
       netmask 255.255.255.0
       gateway 10.7.2.1
```

**Blackbell(255Host)**

```
auto eth0
iface eth0 inet static
       address 10.7.3.2
       netmask 255.255.255.0
       gateway 10.7.3.1

```

**Garden**

```
auto eth0
iface eth0 inet static
       address 10.7.0.26
       netmask 255.255.255.248
       gateway 10.7.0.25
```

**SSS**

```
auto eth0
iface eth0 inet static
       address 10.7.0.27
       netmask 255.255.255.248
       gateway 10.7.0.25
```

  ## Soal C
  
  ***Anya, putri pertama Loid, juga berpesan kepada anda agar melakukan Routing agar setiap perangkat pada jaringan tersebut dapat terhubung.***
  
  ## Soal D
  
  ***Tugas berikutnya adalah memberikan ip pada subnet Forger, Desmond, Blackbell, dan Briar secara dinamis menggunakan bantuan DHCP server. Kemudian kalian ingat bahwa kalian harus setting DHCP Relay pada router yang menghubungkannya.***
  
  ## Soal D1
  
  ***Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Strix menggunakan iptables, tetapi Loid tidak ingin menggunakan MASQUERADE.***
  
  ## Soal D2
  
  ***Kalian diminta untuk melakukan drop semua TCP dan UDP dari luar Topologi kalian pada server yang merupakan DHCP Server demi menjaga keamanan.***
  
  ## Soal D3
  
  ***Loid meminta kalian untuk membatasi DHCP dan DNS Server hanya boleh menerima maksimal 2 koneksi ICMP secara bersamaan menggunakan iptables, selebihnya didrop.***
  
  ## Soal D4
  
  ***Akses menuju Web Server hanya diperbolehkan disaat jam kerja yaitu Senin sampai Jumat pada pukul 07.00 - 16.00.***
  
  ## Soal D5
  
  ***Karena kita memiliki 2 Web Server, Loid ingin Ostania diatur sehingga setiap request dari client yang mengakses Garden dengan port 80 akan didistribusikan secara bergantian pada SSS dan Garden secara berurutan dan request dari client yang mengakses SSS dengan port 443 akan didistribusikan secara bergantian pada Garden dan SSS secara berurutan.***
  
  ## Soal D6
  
  ***Karena Loid ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level.***
  
