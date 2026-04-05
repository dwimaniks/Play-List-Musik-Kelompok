# Play-List-Musik-Kelompok
- Dode
- Manik
- Dirga
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
