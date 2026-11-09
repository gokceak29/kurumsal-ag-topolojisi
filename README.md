# kurumsal-ag-topolojisi
Cisco Packet Tracer kullanılarak tasarlanmış yıldız topoloji (star topology) kurumsal ağ simülasyonu. 

# Kurumsal Ağ Simülasyonu (Star Topoloji & VLAN Yapılandırması) 
## Proje Mimarisi ve Özellikleri
* **Topoloji Tipi:** Yıldız Topoloji (Star Topology)
* **Aktif Cihazlar:** Cisco 2911 Router, Cisco 2960-24TT Switch[cite: 19] ve 4 adet End-Device (PC)[cite: 19].
* **Uygulanan Teknolojiler:** VLAN (Virtual Local Area Network), Subnetting ve Inter-VLAN Routing[cite: 20, 21].

## Ağ Görselleri ve Yapılandırma Adımları 
### 1. Fiziksel ve Mantıksal Ağ Topolojisi
Ağ altyapısının merkezinde konumlandırılan Switch cihazı üzerinden tüm uç birimlerin Router'a bağlandığı yıldız topoloji görünümü: 

<img width="1920" height="1020" alt="Staj-Cisco Packet Tracer Star Topoloji" src="https://github.com/user-attachments/assets/3a51db2c-7b0e-4410-bfb8-e6cf2324af99" />

### 2. Switch Üzerinde VLAN Yapılandırması
Kurumsal ağ güvenliğini ve departman bazlı segmentasyonu sağlamak amacıyla Switch0 cihazı üzerinde "Bilgi_Islem" (VLAN 10) ve "Insan_Kaynaklari" (VLAN 20) sanal ağları tanımlanmıştır[cite: 21]: 

<img width="877" height="888" alt="Star Topoloji Switch Cihazında VLAN Oluşturma" src="https://github.com/user-attachments/assets/14d9ac28-e257-453b-abb2-d6c6421f3348" />

### 3. Router Kapılarının Bölünmesi (Inter-VLAN Routing) ve IP Atamaları
Farklı VLAN'lar arasındaki veri iletişimini sağlamak için Router0 arayüzü alt arayüzlere (sub-interface) bölünmüş ve 192.168.10.0 / 192.168.20.0 ağ blokları tanımlanarak konfigürasyon hafızaya kaydedilmiştir[cite: 20]: 

<img width="1152" height="1020" alt="Star Topoloji Router Kapılarını İkiye Böldü ve IP Adreslerini aldı,  OK  yazısına ulaşıldı (Hafızaya Kaydetti)" src="https://github.com/user-attachments/assets/f4c3ceaa-04af-4c9a-860a-31df5ceb2c34" />

### 4. End-to-End Erişilebilirlik ve Ping Testleri
Ağ yapılandırmasının doğruluğunu test etmek amacıyla farklı alt ağlardaki bilgisayarlar arasında gerçekleştirilen paket iletim (ping) testi başarılı sonuçlanmıştır[cite: 22]:

<img width="877" height="888" alt="Star Topolojinin end-to-end erişilebilirlik testleri (ping) gerçekleştirilmiştir" src="https://github.com/user-attachments/assets/1cbb7b6d-55fd-4d88-b727-ba1ff3d61e01" />

