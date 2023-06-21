# LP12DPBO2023C1
Latihan Praktikum 12 Mata Kuliah Desain dan Pemrograman Berorientasi Objek. Mengubah model arsitektur menjadi MVVM.

Saya Najma Qalbi Dwiharani dengan NIM 2102843 mengerjakan soal LP 12 dalam mata kuliah Desain dan Pemrograman Berorientasi Objek untuk keberkahanNya maka saya tidak melakukan kecurangan seperti yang telah dispesifikasikan. Aamiin.

### Alasan Memilih MVVM

Karena pengguna akan masuk melalui view dan tidak ada kontrak yang mengikat view. Kemudian viewmodel digunakan untuk menghubungkan model dan view dalam melakukan proses bisnis.

## UPDATE

### Model TMD

**Model**
- DB : untuk koneksi database
- PlayerTable : extends DB, untuk mengeksekusi query-query pada tscore dan terhubung ke database
- GameInterface
- GameObject
- Floor : extends GameObject, obstacle untuk lantai yang dipijak
- Player : extends, GameObject, pemain

**ViewModel**
- FloorHandler : untuk proses bisnis banyak Floor seperti membuat, menghapus, merender semua Floor
- PlayerHandler : untuk proses bisnis player seperti menerima inputan key, merender player, mengecek collision player
- TableProcess : untuk penghubung antara view dan model PlayerTable dengan database, mengirim data-data dan membuat data baru
- Game : proses bisnis utama dalam game, akan dipanggil di GameDisplay
- Sound : mengatur backround music dari game

**View**
- GameMenu : menampilkan menu game dan menggunakan TableProcess untuk mengambil data-datanya
- GameDisplay : menampilkan game dan memanggil Game

### Perbedaan Dengan TMD

Sama-sama menggunakan struktur MVVM, namun di TMD Player ada di bagian model dan terdapat PlayerHandler yang ada di viewmodel untuk mengatur Player. Display di TMD menjadi GameDisplay dan menjadi bagian dari view karena pada GameDisplay yang ada di TMD akan memanggil Game. Game menjadi bagian dari viewmodel karena berisi proses bisnis utama dari permainan.
