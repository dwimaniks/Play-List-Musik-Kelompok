# Play-List-Musik-Kelompok
- Dode  (2501010109)
- Manik (2501010107)
- Dirga (2501010116)

# Linked List pada Playlist Musik
# 1. Apa itu Linked List?
### Linked List adalah struktur data yang terdiri dari kumpulan node yang saling terhubung.
### Setiap node berisi:
- Data (misalnya: lagu)
- Pointer / link ke node lain
### 👉 Berbeda dengan array:
- Array → data tersimpan berurutan di memori
- Linked List → data saling terhubung lewat pointer

# 2. Kenapa Playlist Musik Butuh Linked List?
### Bayangkan playlist di aplikasi seperti Spotify:
<img width="3840" height="2040" alt="image" src="https://github.com/user-attachments/assets/ac5ccc2c-ef0e-4b6f-991a-5854afb66d87" />

### Bisa:
- Tambah lagu kapan saja
- Hapus lagu
- Pindah ke lagu berikutnya / sebelumnya
### 👉 Masalah kalau pakai array:
- Tambah di tengah → harus geser data
- Hapus → juga harus geser
### 👉 Solusi:
#### Gunakan Linked List karena lebih fleksibel

# Studi Kasus: Playlist Musik menggunakan Linked List
## Latar Belakang
Pada aplikasi musik seperti Spotify, pengguna diberikan kebebasan untuk mengelola playlist sesuai keinginan. Aktivitas yang sering dilakukan antara lain:
Pada aplikasi seperti Spotify, pengguna dapat:
- Menambahkan lagu baru ke dalam playlist
- Menghapus lagu yang tidak diinginkan
- Memutar lagu berikutnya (next) atau sebelumnya (previous)

### Hal ini menunjukkan bahwa data playlist bersifat dinamis, artinya:
- Jumlah lagu bisa bertambah atau berkurang kapan saja
- Urutan lagu bisa berubah sesuai kebutuhan pengguna

### Permasalahan
Jika menggunakan array:
- Menambah lagu di tengah → harus geser data
- Menghapus lagu → harus geser juga
- Kurang efisien untuk playlist besar

### Solusi: Linked List
Gunakan doubly linked list:
#### Setiap lagu = node
- Node punya:
- data (judul lagu)
- next (lagu berikutnya)
- prev (lagu sebelumnya)
##### 👉 Struktur:
###### NULL ← Lagu A ⇄ Lagu B ⇄ Lagu C → NULL
<img width="1160" height="502" alt="image" src="https://github.com/user-attachments/assets/10cbe34f-dd9a-4468-83a0-b4ceab5669eb" />

### Alur Studi Kasus
1. Menambahkan Lagu
##### Misal tambah “Lagu D” setelah Lagu B:
###### A ⇄ B ⇄ C  
###### ↓  
###### A ⇄ B ⇄ D ⇄ C
✔ Hanya ubah pointer, tidak geser dat
2. Menghapus Lagu
##### Hapus Lagu B:
###### A ⇄ B ⇄ C  
###### ↓  
###### A ⇄ C
✔ Node B dilepas, node lain tetap
3. Navigasi Lagu
##### Next → pindah ke next
##### Previous → pindah ke prev
##### 👉 Contoh:
###### Sedang di Lagu B → next = Lagu C
###### Previous = Lagu A
4. Saat Lagu Diputar
##### Sistem menyimpan current node
###### Saat lagu selesai → pindah ke node berikutnya
<img width="2048" height="2048" alt="image" src="https://github.com/user-attachments/assets/05edeca9-75e3-4f99-91cc-31d63f4900d3" />

### Keuntungan Solusi
- Fleksibel (data bisa berubah kapan saja)
- Efisien (tidak perlu geser data)
- Mendukung fitur next/previous
- Cocok untuk playlist besar


## Rumusan Masalah
1. Bagaimana cara mengelola data playlist musik yang bersifat dinamis (tambah dan hapus lagu)?
2. Bagaimana struktur linked list dapat digunakan untuk merepresentasikan urutan lagu dalam playlist?
3. Bagaimana proses navigasi lagu (next dan previous) dapat dilakukan secara efisien?
4. Bagaimana cara menyisipkan lagu di posisi tertentu tanpa mengganggu urutan playlist?
5. Bagaimana cara menghapus lagu dari playlist tanpa harus menggeser data seperti pada array?
6. Mengapa linked list lebih efektif dibandingkan array dalam pengelolaan playlist musik?

## implementasi playlist musik menggunakan Doubly Linked List (Python)
### Konsep
#### Setiap lagu = Node
#### Punya:
- prev → lagu sebelumnya
- next → lagu berikutnya

## Kesimpulan
### Berdasarkan studi kasus playlist musik menggunakan linked list, dapat disimpulkan bahwa:
- Linked list merupakan struktur data yang sangat cocok untuk mengelola playlist karena bersifat dinamis (mudah menambah dan menghapus lagu).
- Dengan menggunakan doubly linked list, navigasi lagu menjadi lebih mudah karena dapat berpindah ke lagu berikutnya (next) dan lagu sebelumnya (prev).
- Proses penambahan dan penghapusan lagu lebih efisien dibandingkan array karena tidak perlu menggeser data.
- Linked list mampu merepresentasikan urutan lagu secara terstruktur dan fleksibel.
- Implementasi ini banyak digunakan pada aplikasi nyata seperti Spotify dan YouTube.

# CONTOH FOTO LINKED LIST PADA PLAYLIST MUSIK
<img width="1080" height="2400" alt="image" src="https://github.com/user-attachments/assets/ce2bb6e1-ca19-47d8-bfbc-d442305e8fc5" />

<img width="2048" height="2048" alt="image" src="https://github.com/user-attachments/assets/05edeca9-75e3-4f99-91cc-31d63f4900d3" />
