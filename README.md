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
  
  
 - SETTING INTERFACE PADA GNS3
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
  
  ## Soal C
  
  ## Soal D
  
  ## Soal D1
  
  ## Soal D2
  
  ## Soal D3
  
  ## Soal D4
  
  ## Soal D5
  
  ## Soal D6
  
