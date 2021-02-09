# Jawab_Soal

1. Linear Layout
   Linear Layout adalah jenis layout dimana user menempatkan 1 objek per baris atau kolom secara sejajar. Jadi di dalam setiap baris atau kolom hanya ada 1 objek yang              bisa ditempatkan . Linear Layout ini ada dua jenis . Yaitu :
   Linear Layout Vertical (Objek per baris/kesamping) 
   Linear Layout Horizontal (Objek per kolom/kebawah)
2. Relative Layout
   Relative Layout adalah jenis layout yang memiliki karakteristik dalam menempatkan view secara relatif (Baca apa itu relatif disini). Relatif disini berarti posisi dari setiap    view bergantung kepada view yang lain. Simplenya adalah, kita bebas untuk menempatkan objek yang diinginkan sesuka hati kita. Penempatan satu objek bisa dimana saja mau di      sisi kanan, kiri, atas, ataupun bawah dari objek lain.
3. Constraint Layout
   Constarint Layout memungkinkan kita membuat tata letak yang besar dan kompleks dengan tampilan datar. Ini hampir mirip dengan Relative Layout karena semua tampilan ditata        berdasarkan hubungan antara satu objek dengan yang lain, tetapi lebih fleksibel daripada RelativeLayout dan lebih mudah digunakan dengan Editor Layout Android Studio.
   
   
-Kesimpulan
   Dari ketiga layout tersebut maka kita bisa mengambil kesimpulan bahwa setiaplayout memiliki keunggulan dan kekurangan masing-masing, linear layout bisa mengikuti ukuran layar    handphone yang berbeda-beda tanpa merubah susuan objek, relative layout hanya akan terlihat sesuai dengan apa yang telah ditetapkan sebelumnya jika ukuran layar berubah bisa    saja objek ada yang terpotong atau bahkan tidak terlihat, sedangkan constraint layout itu lebih flexible dan mudah untuk dibuat.

-onCreate()
   adalah kondisi awal saat Activity baru diciptakan, biasanya dilakukan inisialisasi pada tahapan ini.Anda harus menerapkan callback ini, yang aktif saat sistem pertama kali      membuat aktivitas. Pada pembuatan aktivitas, aktivitas memasuki status Dibuat. Dalam metode onCreate(), Anda menjalankan logika startup aplikasi dasar yang hanya boleh          terjadi sekali selama siklus aktivitas. Misalnya, implementasi onCreate() mungkin mengikat data ke daftar, mengaitkan aktivitas dengan ViewModel, dan membuat instance            beberapa variabel lingkup class. Metode ini menerima parameter savedInstanceState, yang merupakan objek Bundle yang berisi status aktivitas yang sebelumnya disimpan. Jika        aktivitas belum pernah ada sebelumnya, nilai objek Bundle adalah nol.
   Jika Anda memiliki komponen berbasis siklus proses yang terhubung dengan siklus proses aktivitas Anda, aktivitas akan menerima peristiwa ON_CREATE. Metode yang dijelaskan        dengan @OnLifecycleEvent akan dipanggil sehingga komponen berbasis siklus proses Anda dapat melakukan kode penyiapan apa pun yang diperlukan untuk status yang dibuat.

-onPause()
   akan dipanggil saat ada Activity lain yang terbuka.Sistem akan memanggil metode ini sebagai indikasi pertama bahwa pengguna meninggalkan aktivitas Anda (meskipun tidak selalu    berarti aktivitas sedang ditutup); hal ini menunjukkan bahwa aktivitas tidak lagi di latar depan (meskipun mungkin masih terlihat jika pengguna berada dalam mode multi-          jendela). Gunakan metode onPause() untuk menjeda atau menyesuaikan operasi yang tidak boleh dilanjutkan (atau harus dilanjutkan dalam jumlah sedang) sementara Activity berada    dalam status Dijeda, dan Anda berharap untuk segera melanjutkan. Ada beberapa alasan mengapa suatu aktivitas dapat memasuki status ini. Contoh:
   Beberapa acara mengganggu eksekusi aplikasi, seperti yang dijelaskan pada bagian onResume(). Ini adalah kasus yang paling umum.
   Di Android 7.0 (API level 24) atau lebih tinggi, beberapa aplikasi berjalan dalam mode multi-jendela. Karena hanya satu aplikasi (jendela) yang memiliki fokus di setiap          waktu, sistem menjeda semua aplikasi lain.
   Aktivitas semi-transparan baru (seperti dialog) terbuka. Selama aktivitas masih terlihat sebagian tetapi tidak dalam fokus, aktivitas tersebut tetap dijeda.
   Saat aktivitas berpindah ke status dijeda, komponen berbasis siklus proses yang terkait dengan siklus proses aktivitas akan menerima peristiwa ON_PAUSE. Di sinilah komponen      siklus proses dapat menghentikan fungsi apa pun yang tidak perlu dijalankan saat komponen tidak ada di latar depan, seperti menghentikan pratinjau kamera.
   Anda juga dapat menggunakan metode onPause() untuk melepaskan resource sistem, menangani sensor (seperti GPS), atau resource apa pun yang dapat memengaruhi masa pakai baterai    saat aktivitas Anda dijeda dan pengguna tidak membutuhkannya. Namun, seperti yang disebutkan di atas di bagian onResume(), aktivitas yang Dijeda mungkin masih sepenuhnya        terlihat jika berada dalam mode multi-jendela. Karena itu, Anda harus mempertimbangkan menggunakan onStop() daripada onPause() untuk sepenuhnya melepaskan atau menyesuaikan      resource dan operasi terkait UI untuk lebih optimal mendukung mode multi-jendela.
