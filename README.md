# organisasi-dan-struktur-data
# Organisasi Struktur Data

nama: Pelangilarasati
Nim: 09011382429...
kelas: SKU2B
## 1. Arsitektur Interkoneksi dalam Sistem Komputer: Struktur dan Implementasi
Arsitektur interkoneksi merupakan aspek fundamental dalam desain sistem komputer, yang mendefinisikan mekanisme komunikasi dan pertukaran data antar komponen-komponen esensial seperti Unit Pemrosesan Pusat (CPU), memori, dan perangkat Input/Output (I/O).
 * Bus Sistem:
   * Jalur komunikasi terpadu yang memfasilitasi transfer data antar komponen.
   * Contoh implementasi: Bus PCI Express (PCIe) yang menghubungkan kartu grafis dan perangkat berkinerja tinggi lainnya ke papan induk.
 * Hierarki Bus:
   * Mengimplementasikan lapisan-lapisan bus dengan kecepatan dan bandwidth yang berbeda untuk optimasi kinerja.
   * Contoh implementasi: Arsitektur Northbridge/Southbridge pada papan induk konvensional, di mana Northbridge menangani komunikasi berkecepatan tinggi antara CPU dan memori, sementara Southbridge menangani perangkat I/O yang lebih lambat.
 * Interkoneksi Berbasis Switching:
   * Memanfaatkan switch untuk menciptakan jalur komunikasi dinamis dan efisien antar perangkat.
   * Contoh implementasi: Jaringan Mesh pada sistem Multi prosesor.
 * Interkoneksi Point-to-Point:
   * Menyediakan jalur komunikasi khusus antara dua komponen, meminimalkan latensi dan memaksimalkan throughput.
   * Contoh implementasi: HyperTransport dan QuickPath Interconnect (QPI) yang diimplementasikan dalam arsitektur CPU tertentu.
## 2. Faktor-faktor yang Mempengaruhi Degradasi Kinerja Bus pada Beban Tinggi
Peningkatan jumlah modul atau perangkat yang terhubung pada bus dapat mengakibatkan penurunan kinerja yang signifikan, yang terutama disebabkan oleh:
 * Kontensi Bus:
   * Peningkatan jumlah perangkat meningkatkan probabilitas terjadinya perebutan akses bus, yang menyebabkan penundaan dan penurunan efisiensi.
   * Hal ini dapat dianalogikan dengan kepadatan lalu lintas pada jalur transportasi.
 * Batasan Bandwidth:
   * Setiap bus memiliki kapasitas bandwidth maksimum. Ketika beban data melebihi kapasitas ini, terjadi saturasi bus, yang mengakibatkan antrian dan penundaan.
 * Efek Propagasi Sinyal:
   * Peningkatan panjang jalur bus dan jumlah koneksi dapat menyebabkan distorsi sinyal, yang memerlukan mekanisme koreksi kesalahan dan transmisi ulang, sehingga mengurangi throughput efektif.
## 3. Mekanisme Prioritas Bus dan Anomali Waktu Tunggu
 * Dalam sistem bus dengan mekanisme prioritas, perangkat dengan prioritas rendah umumnya memiliki waktu tunggu rata-rata yang lebih singkat karena mereka hanya mendapatkan akses bus ketika perangkat dengan prioritas tinggi tidak aktif.
 * Alasan Perangkat prioritas rendah mendapat waktu tunggu rendah.
   * Perangkat dengan prioritas rendah akan mendapatkan kesempatan untuk mentransmisikan data, disaat perangkat dengan prioritas tinggi tidak melakukan transmisi data, sehingga waktu tunggu yang didapatkan akan menjadi lebih rendah.
 * Kondisi pengecualian:
   * Jika perangkat dengan prioritas tinggi terus-menerus mendominasi bus, perangkat dengan prioritas rendah dapat mengalami kondisi kelaparan (starvation), di mana mereka tidak pernah mendapatkan akses bus.
   * Jika terjadi kesalahan pada mekanisme arbitrase bus, prioritas dapat diabaikan, yang mengakibatkan perilaku yang tidak dapat diprediksi.
