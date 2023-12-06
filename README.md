# Jarkom-Modul-4-IT11-2023

#### Anggota Kelompok A11:

| Nama                   | NRP        |
| ---------------------- | ---------- |
| Midyanisa Yuniar       | 5027211025 |
| Dyas Amorita Radhwa N  | 5027211009 |

> Prefiks IP kelompok A11 -> 10.69

# Daftar Isi
* [Topologi](#Topologi)
* [CPT VLSM](#CPT-VLSM)
* [Tree VSLM](#Tree-VSLM)
* [GNS3 CIDR](#GNS3-CIDR)
* [Penggabungan CIDR](#Penggabungan-CIDR)
* [Tree CIDR](#Tree-CIDR)
  
# Topologi
Berikut adalah topologi dari soal yang akan kami buat di **Cicso Packet Tracer** dan **GNS3**

![Topologi_Soal](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/1a020418-2d0c-44a6-8c17-94a103bcaeb1)

Berikut adalah topologi yang kami gunakan, disini kami menggunakan topologi yang sama pada **CPT: VSLM** dan **GNS#: CIDR**

![A](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/175b80b0-5bf7-4b16-83ab-deb7ff9bc1f8)


Kemudian Berikut adalah daftar Netmask berdasarkan topologi yang sudah dibuat

![Netmask_umum](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/e42fb609-72a8-4562-88a6-ed20e74fb379)


# CPT VLSM

## Tree VSLM

# GNS3 CIDR
## Penggabungan CIDR

Sebelum melakukan subnetting pada ip, dilakukan penggabungan terlebih dahulu. Berikut ini merupakan langkah dalam penggabungan tersebut

### **Langkah 1**

![A](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/50ffe82d-223c-454c-b687-c25f2375e43b)


### **Langkah 1**

![B](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/da1792ac-b510-4a83-9261-511ac635f253)


### **Langkah 2**

![C](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/fe6388c8-2ebf-4ab5-b258-eeda456ba09a)


### **Langkah 3**

![D](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/e86829b0-dd6e-42d7-8394-b8b26d52eb66)


### **Langkah 4**

![E](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/1fe46a46-750e-4320-9b15-80b66cebaaab)


### **Langkah 5**

![F](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/1d623ffe-ebd0-4272-b344-997a293f75f5)


### **Langkah 6**

![G](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/1e05b6ea-d1c1-42e2-8d9a-c8690661d406)


### **Langkah 7**

![H](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/7f7d5ad0-a795-482c-b311-041cc0d88028)


### **Langkah 8**

![I](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/0ea17466-c8ce-4698-9358-246f3530f5ab)

Kemudian berikut ini merupakan tabel subnetting berdasarkan penggabungan yang sudah dilakukan

![1_2](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/a14a8f5a-02a1-4e7e-bc9e-867ca25227d7)

![3_4](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/afbe6b7a-e539-45f4-9894-46ed2c89c764)

![5_6](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/1b80fa5d-078a-4f9b-8e47-3aad9696adf0)

![image](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/3b38e96c-e96b-45f7-9242-0878c6717777)

### Tree CIDR

Berdasarkan penggabungan yang sudah dilakukan berikut adalah tree subnetting dari CIDR

![tree_CIDR](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/0903de34-73f9-44ee-a8ad-8296c16b0a42)

### Hasil Pembagian Subnet

Berdasarkan Tree, didpatkan pembagian subnet sebagai berikut

![pembagian_subnet](https://github.com/Yuniarrr/Jarkom-Modul-4-IT11-2023/assets/107184933/b1042a1a-a9ee-4e94-97be-d0b34334a26f)


### Konfigurasi pada GNS

#### Client

- **Royal Capital**

```
  auto eth0
  iface eth0 inet static
  	address 10.70.0.2
  	netmask 255.255.255.0
  	gateway 10.70.0.1
```

- **Wille Region**

```
auto eth0
iface eth0 inet static
	address 10.70.0.3
	netmask 255.255.255.0
	gateway 10.70.0.1
```

- **Turk Region**

```
auto eth0
iface eth0 inet static
	address 10.69.0.2
	netmask 255.255.252.0
	gateway 10.69.0.1
```

- **Grobe Forest**

```
auto eth0
iface eth0 inet static
	address 10.69.4.2
	netmask 255.255.255.0
	gateway 10.69.4.1
```

- **Granz Channel**

```
auto eth0
iface eth0 inet static
	address 10.69.34.2
	netmask 255.255.254.0
	gateway 10.69.34.1

```

- **Bred Region**

```
auto eth0
iface eth0 inet static
	address 10.69.40.2
	netmask 255.255.255.252
	gateway 10.69.40.1
```

- **Riegel Canyon**

```
auto eth0
iface eth0 inet static
	address 10.69.36.3
	netmask 255.255.252.0
	gateway 10.69.36.1
```

- **Lake Corridor**

```
auto eth0
iface eth0 inet static
	address 10.71.64.2
	netmask 255.255.255.224
	gateway 10.71.64.1
```

- **Appetit Region**

```
auto eth0
iface eth0 inet static
	address 10.71.8.2
	netmask 255.255.248.0
	gateway 10.71.8.1
```

- **Laub Hills**

```
auto eth0
iface eth0 inet static
	address 10.71.8.3
	netmask 255.255.248.0
	gateway 10.71.8.1
```

- **Schwer Mountains**

```
auto eth0
iface eth0 inet static
	address 10.71.0.6
	netmask 255.255.255.248
	gateway 10.71.0.5
```

- **Rohr Road**

```
auto eth0
iface eth0 inet static
	address 10.71.0.18
	netmask 255.255.252.0
	gateway 10.71.0.17
```

#### **Gateway**

- **Aura**

```
auto eth0
iface eth0 inet dhcp

#A4
auto eth1
iface eth1 inet static
  address 10.70.1.2
  netmask 255.255.255.252

#A7
auto eth2
iface eth2 inet static
  address 10.69.128.1
  netmask 255.255.255.252

#A14
auto eth3
iface eth3 inet static
  address 10.71.128.2
  netmask 255.255.255.252
```

- **Denken**

```
auto eth0
iface eth0 inet static
  address 10.70.1.1
  netmask 255.255.255.252

#A1
auto eth1
iface eth1 inet static
  address 10.70.0.1
  netmask 255.255.255.0
```

- **Eisen**

```
#A7
auto eth0
iface eth0 inet static
  address 10.69.128.2
  netmask 255.255.255.252

#A5
auto eth1
iface eth1 inet static
  address 10.69.16.1
  netmask 255.255.255.252

#A6
auto eth2
iface eth2 inet static
  address 10.69.8.1
  netmask 255.255.255.252

#A8
auto eth3
iface eth3 inet static
  address 10.69.48.1
  netmask 255.255.255.252

#A13
auto eth4
iface eth4 inet static
  address 10.69.64.1
  netmask 255.255.255.248
```

- **Fern**

```
#Fern
#A17
auto eth0
iface eth0 inet static
  address 10.71.16.2
  netmask 255.255.255.252

#A18
auto eth1
iface eth1 inet static
  address 10.71.8.1
  netmask 255.255.248.0
```

- **Flamme**

```
#Flamme
#A16
auto eth0
iface eth0 inet static
  address 10.71.32.2
  netmask 255.255.255.252

#A19
auto eth1
iface eth1 inet static
  address 10.71.0.1
  netmask 255.255.255.252

#A17
auto eth2
iface eth2 inet static
  address 10.71.16.1
  netmask 255.255.255.252

#A21
auto eth3
iface eth3 inet static
  address 10.71.0.17
  netmask 255.255.252.0
```

- **Frieren**

```
#Frieren
#A14
auto eth0
iface eth0 inet static
  address 10.71.128.3
  netmask 255.255.255.252

#A15
auto eth1
iface eth1 inet static
  address 10.71.64.1
  netmask 255.255.255.224

#A4
auto eth2
iface eth2 inet static
  address 10.71.32.1
  netmask 255.255.255.252
```

- **Heiter**

```
#A11
auto eth0
iface eth0 inet static
	address 10.69.40.3
	netmask 255.255.255.252

#A12
auto eth1
iface eth1 inet static
  address 10.69.36.1
  netmask 255.255.252.0
```

- **Himmel**

```
#A19
auto eth0
iface eth0 inet static
  address 10.71.0.2
  netmask 255.255.255.252

#A20
auto eth1
iface eth1 inet static
  address 10.71.0.5
  netmask 255.255.255.248
```

- **Lawine**

```
#A10
auto eth0
iface eth0 inet static
  address 10.69.32.2
  netmask 255.255.255.252

#A11
auto eth1
iface eth1 inet static
  address 10.69.40.1
  netmask 255.255.255.252
```

- **Linie**

```
#A8
auto eth0
iface eth0 inet static
  address 10.69.48.2
  netmask 255.255.255.252

#A9
auto eth1
iface eth1 inet static
  address 10.69.34.1
  netmask 255.255.254.0

#A10
auto eth2
iface eth2 inet static
  address 10.69.32.1
  netmask 255.255.255.252
```

- **Lugner**

```
#A6
auto eth0
iface eth0 inet static
  address 10.69.8.2
  netmask 255.255.255.252

#A2
auto eth1
iface eth1 inet static
  address 10.69.0.1
  netmask 255.255.252.0

#A3
auto eth2
iface eth2 inet static
  address 10.69.4.1
  netmask 255.255.255.0
```

#### **Server**

- **Stark**

```
auto eth0
iface eth0 inet static
	address 10.69.16.2
	netmask 255.255.255.252
	gateway 10.69.16.1
```

- **Sein**

```
auto eth0
iface eth0 inet static
	address 10.69.36.2
	netmask 255.255.252.0
	gateway 10.69.36.1
```

- **Revolte**

```
auto eth0
iface eth0 inet static
	address 10.69.64.2
	netmask 255.255.255.248
	gateway 10.69.64.1
```

- **Reichter**

```
auto eth0
iface eth0 inet static
	address 10.69.64.3
	netmask 255.255.255.248
	gateway 10.69.64.1
```

### **Routing**

Kemudian Konfigurasi routing pada terminal dari tiap gateway

- **Denken**

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.70.1.2
```

- **Heiter**

```
route add -net 10.69.36.0 netmask 255.255.252.0 gw 10.69.36.1
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.69.40.1
```

- **Lawine**

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.69.32.1
route add -net 10.69.36.0 netmask 255.255.252.0 gw 10.69.40.3
```

- **Himmel**

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.71.0.1
```

- **Aura**

```
route add -net 10.70.0.0 netmask 255.255.255.0 gw 10.70.1.1
route add -net 10.69.0.0 netmask 255.255.252.0 gw 10.69.128.2
route add -net 10.69.4.0 netmask 255.255.255.0 gw 10.69.128.2
route add -net 10.69.34.0 netmask 255.255.254.0 gw 10.69.128.2
route add -net 10.69.36.0 netmask 255.255.252.0 gw 10.69.128.2
route add -net 10.69.40.0 netmask 255.255.255.252 gw 10.69.128.2
route add -net 10.69.16.0 netmask 255.255.255.252 gw 10.69.128.2
route add -net 10.69.64.0 netmask 255.255.255.248 gw 10.69.128.2
route add -net 10.71.64.0 netmask 255.255.255.224 gw 10.71.128.3
route add -net 10.71.8.0 netmask 255.255.248.0 gw 10.71.128.3
route add -net 10.71.0.16 netmask 255.255.252.0 gw 10.71.128.3
route add -net 10.71.0.4 netmask 255.255.252.0 gw 10.71.128.3
```

- **Eisen**

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.69.128.1
route add -net 10.69.0.0 netmask 255.255.252.0 gw 10.69.8.2
route add -net 10.69.4.0 netmask 255.255.255.0 gw 10.69.8.2
route add -net 10.69.34.0 netmask 255.255.254.0 gw 10.69.48.2
```

- **Frieren**

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.71.128.2
route add -net 10.71.8.0 netmask 255.255.248.0 gw 10.71.32.2
route add -net 10.71.0.16 netmask 255.255.252.0 gw 10.71.32.2
route add -net 10.71.0.4 netmask 255.255.255.248 gw 10.71.32.2
```

- **Lugner**

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.69.8.1
```

- **Fern**

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.71.16.1
```

- **Linie**

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.69.48.1
route add -net 10.69.36.0 netmask 255.255.252.0 gw 10.69.32.1
route add -net 10.69.40.0 netmask 255.255.255.252 gw 10.69.32.1
route add -net 10.69.36.0 netmask 255.255.252.0 gw 10.69.48.1
route add -net 10.69.40.0 netmask 255.255.255.252 gw 10.69.48.1
```

- **Flamme**

```
route add -net 10.71.8.0 netmask 255.255.248.0 gw 10.71.16.2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.71.32.1
route add -net 10.71.0.4 netmask 255.255.255.248 gw 10.71.0.2
```


sebentar masih aku rapiin di readme lain



