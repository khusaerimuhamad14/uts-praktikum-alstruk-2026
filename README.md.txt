# Tugas Praktikum Struktur Data - Kelas D

Dokumen ini berisi penjelasan mengenai dua program C++ yang telah diimplementasikan untuk memenuhi tugas praktikum. Program pertama berfokus pada manajemen data mahasiswa menggunakan `struct` dan `array`, sedangkan program kedua mensimulasikan struktur data dasar *Stack* dan *Queue*.

## Identitas Mahasiswa
* **Nama:** Muhamad Khusaeri
* **NIM:** 2503010090
* **Kelas:** D

---

## Penjelasan Jalannya Program

**1. Program Manajemen Data Mahasiswa (`2503010090_MUHAMAD KHUSAERI_1_ab.cpp`)** Program ini dibuat untuk mencatat, mengolah, dan menampilkan data mahasiswa secara dinamis dengan kapasitas maksimal 5 mahasiswa menggunakan konsep `struct` (tipe data bentukan) bernama `Mahasiswa` yang mengemas variabel `nim`, `nama` bertipe *string*, `semester` bertipe *integer*, dan `ipk` bertipe *float* ke dalam satu kesatuan objek. Dalam proses pembuatannya, program ini memanfaatkan pustaka standar `<iostream>` untuk menangani proses input-output data melalui fungsi `cin` dan `cout`, fungsi `cin.ignore()` bersama `getline()` agar input nama mahasiswa yang menggunakan spasi tidak terpotong, serta pustaka `<iomanip>` menggunakan fungsi manipulator `setw()`, `left`, `fixed`, dan `setprecision(2)` untuk memformat visualisasi keluaran data mahasiswa agar tersusun menjadi bentuk tabel yang rapi, presisi, dan sejajar pada layar *console*. Alur logika program ini dilengkapi dengan struktur kontrol perulangan (*looping for*) dan percabangan (*conditional if*) untuk melakukan penginputan data secara berulang sesuai jumlah mahasiswa yang diinginkan, melakukan pemindaian (*scanning*) untuk menyaring dan mencari mahasiswa dengan perolehan IPK tertinggi, menghitung nilai rata-rata IPK dari seluruh data yang masuk dengan rumus pembagian total nilai, serta menjalankan fitur filter pencarian berbasis kondisi logika boolean (`bool temukan`) untuk mencocokkan dan menampilkan baris data mahasiswa yang berada di semester tertentu sesuai dengan instruksi input dari pengguna.

**2. Program Simulasi Stack dan Queue (`khusaerisoal2AB.cpp`)** Program ini berisi simulasi dari dua konsep struktur data linear yang fundamental dalam ilmu komputer menggunakan media penyimpanan berupa array statis global berkapasitas 5 elemen dengan memanfaatkan pustaka `<iostream>` untuk mencetak hasil simulasi ke layar serta pustaka `<string>` untuk menampung data teks. Pada bagian pertama, program mensimulasikan struktur data **Stack (Tumpukan Buku)** bertipe *string* bernama `stackArr` yang bekerja menggunakan prinsip operasi *LIFO (Last In, First Out)* dengan dikendalikan oleh variabel indeks `top` (diinisialisasi bernilai -1), di mana program ini mengimplementasikan fungsi kondisi `stackEmpty()` dan `stackFull()`, operasi `push()` untuk menambah judul buku ke tumpukan paling atas dengan mekanisme *pre-increment* (`++top`), operasi `pop()` untuk menghapus sekaligus menurunkan posisi tumpukan dengan fungsi *post-decrement* (`top--`), fungsi `peekStack()` untuk mengintip elemen teratas tanpa menghapusnya, serta fungsi `tampilStack()` menggunakan perulangan menurun (*decrementing loop*) untuk menampilkan tumpukan buku dari atas ke bawah. Pada bagian kedua, program mensimulasikan struktur data **Queue (Antrean Perpustakaan)** bertipe *string* bernama `queueArr` yang bekerja menggunakan prinsip operasi *FIFO (First In, First Out)* dengan dikendalikan oleh variabel penunjuk indeks `qFront` (depan), `qRear` (belakang), dan variabel `jumlah` untuk melacak total antrean aktif, di mana program ini mengimplementasikan metode *Circular Queue* (antrean melingkar) menggunakan rumus operasi sisa bagi atau modulus (`(index + 1) % 5`) agar pergerakan elemen antrean dapat memanfaatkan slot kosong pada array secara efisien melalui fungsi `enqueue()` untuk memasukkan nama anggota baru dari belakang, fungsi `dequeue()` untuk mengeluarkan atau melayani anggota dari posisi paling depan antrean, fungsi `peekQueue()` untuk melihat anggota terdepan, serta fungsi `tampilQueue()` untuk mencetak seluruh daftar antrean secara berurutan dari depan ke belakang ke layar *console*.

---

## Cara Menjalankan Program

1. Buat sebuah folder bernama `pengumpulan kelas d` di komputer Anda.
2. Masukkan file kode program (`2503010090_MUHAMAD KHUSAERI_1_ab.cpp` dan `khusaerisoal2AB.cpp`) serta file `README.md` ini ke dalam folder tersebut.
3. Buka terminal atau *command prompt* di dalam direktori folder tersebut.
4. Lakukan kompilasi menggunakan *compiler* C++:
   * Kompilasi Program 1: `g++ 2503010090_MUHAMAD KHUSAERI_1_ab.cpp -o program1`
   * Kompilasi Program 2: `g++ khusaerisoal2AB.cpp -o program2`
5. Jalankan program yang telah dikompilasi (`program1` atau `program2`).