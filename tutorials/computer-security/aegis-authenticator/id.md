---
name: Aegis Authenticator
description: Bagaimana cara menggunakan Aegis Authenticator untuk mengamankan akun Anda dengan autentikasi ganda?
---

![cover](assets/cover.webp)

Saat ini, autentikasi dua faktor (2FA) sangat penting untuk mengamankan akun online Anda. Selain kata sandi (password), 2FA menambahkan faktor kedua (biasanya berupa kode 6 angka) yang kedaluwarsa setiap 30 detik. Ini membuat peretas jauh lebih sulit untuk membobol akun Anda. Menggunakan aplikasi TOTP (*Time-based One-Time Password*) khusus jauh lebih aman daripada SMS, yang bisa dibajak melalui serangan SIM swapping (pengambilalihan kartu SIM).

Namun, tidak semua aplikasi autentikasi sama. Banyak solusi eksklusif (Google Authenticator, Authy, dll.) memiliki masalah: mereka bersifat tertutup (closed-source), sehingga mustahil untuk mengaudit keamanannya. Aplikasi tersebut terkadang menyisipkan pelacak iklan, tidak menyediakan pencadangan (backup) terenkripsi, dan bahkan bisa mencegah Anda mengekspor akun untuk mengunci Anda dalam ekosistem mereka.

Aegis Authenticator hadir sebagai alternatif gratis dan etis dari aplikasi-aplikasi tersebut. Aegis adalah aplikasi open-source yang gratis dan aman untuk mengelola token verifikasi dua langkah Anda di Android. Pengembangannya berfokus pada fitur-fitur penting yang tidak ditawarkan aplikasi lain, termasuk enkripsi kuat untuk data lokal dan opsi pencadangan yang aman. Singkatnya, Aegis menawarkan solusi autentikasi ganda yang disimpan secara lokal dan dapat diaudit, ideal bagi siapa saja yang ingin memegang kendali penuh atas kode 2FA mereka.

## Memperkenalkan Aegis Authenticator

Aegis Authenticator merupakan aplikasi 2FA sumber terbuka untuk Android, dirilis di bawah lisensi GPL v3. Aplikasi ini menonjol karena filosofi "privasi sesuai desain": aplikasi ini bekerja sepenuhnya secara offline dan tidak memerlukan koneksi ke layanan jarak jauh. Hasilnya, token Anda tetap tersimpan secara lokal pada perangkat Anda, dalam brankas yang aman dan hanya Anda yang memegang kuncinya.

Aegis Authenticator adalah aplikasi 2FA sumber terbuka untuk Android, dirilis di bawah lisensi GPL v3. Aplikasi ini menonjol karena filosofi "privacy by design": aplikasi berfungsi sepenuhnya secara luring (offline) dan tidak memerlukan koneksi ke layanan jarak jauh. Hasilnya, token Anda tetap tersimpan secara lokal di perangkat Anda, dalam brankas aman yang kuncinya hanya dipegang oleh Anda.

### Fitur utama

**Brankas Terenkripsi:** Semua kode OTP Anda disimpan dalam brankas yang dienkripsi dengan standar AES-256 (mode GCM), dilindungi oleh kata sandi utama (master password) yang Anda buat. Brankas ini bisa dibuka menggunakan password atau data biometrik (sidik jari, pengenalan wajah) untuk kemudahan. Jika Anda tidak mengatur password, data akan tersimpan tanpa enkripsi, jadi kami sangat menyarankan untuk mengaturnya.

**Pengorganisasian Canggih:** Aegis menjaga banyak akun 2FA Anda tetap rapi. Anda bisa mengurutkan entri berdasarkan abjad atau urutan yang Anda suka, mengelompokkannya berdasarkan kategori (misalnya Pribadi, Pekerjaan, Sosial) untuk memudahkan pencarian, dan memberikan ikon khusus pada setiap entri. Kolom pencarian juga tersedia untuk menemukan layanan atau akun berdasarkan nama secara instan.

**Cadangan Lokal Terenkripsi:** Untuk memastikan Anda tidak pernah kehilangan akses ke akun, Aegis menawarkan fitur pencadangan otomatis pada brankas Anda. Cadangan ini terenkripsi (menggunakan kata sandi) dan dapat disimpan di lokasi pilihan Anda (penyimpanan internal, folder cloud, dll.). Aplikasi ini juga bisa mengekspor database akun Anda secara manual, dalam format terenkripsi atau tidak terenkripsi sesuai kebutuhan. Mengimpor akun dari aplikasi 2FA lain juga sangat mudah (Aegis mendukung impor dari Authy, Google Authenticator, FreeOTP, andOTP, dll.).

**Keamanan dan Privasi:** Aplikasi ini sepenuhnya offline secara bawaan. Aegis tidak memerlukan izin jaringan—artinya aplikasi tidak mengirimkan data apa pun ke dunia luar—dan tidak memiliki pelacak iklan atau modul analisis perilaku. Aegis tidak menampilkan iklan dan tidak memerlukan akun pengguna: setelah diinstal, aplikasi langsung bisa digunakan tanpa registrasi. Karena source codenya publik di GitHub, komunitas dapat mengauditnya secara bebas, menjamin tidak adanya fungsi berbahaya atau tersembunyi.

**Interface Modern:** Aegis mengadopsi Material Design yang rapi, dengan dukungan tema gelap (dark theme) (termasuk mode AMOLED), dan bahkan tampilan tile opsional untuk menampilkan kode Anda dalam bentuk kisi. Interfacenya bersih, tanpa fitur yang tidak perlu, dan memblokir tangkapan layar (screenshot) pada kode sebagai langkah keamanan.

## Instalasi

Karena Aegis Authenticator bersifat open source, para pengembangnya lebih mengutamakan saluran distribusi yang ramah privasi. Ada dua cara utama untuk menginstalnya:

### Melalui F-Droid (disarankan)

Cara yang paling aman dan mudah adalah melalui F-Droid, toko alternatif gratis. Jika F-Droid belum terinstal di ponsel Anda, mulailah dengan mengunduhnya dari situs web resmi [F-Droid.org](https://f-droid.org). Kemudian :

- Buka F-Droid dan pastikan Anda telah memperbarui repositori untuk mendapatkan daftar aplikasi terbaru.
- Cari "Aegis Authenticator" di F-Droid. Aplikasi resmi akan muncul (penerbit: Beem Development).
- Mulai instalasi dengan menekan Install. Karena Aegis adalah salah satu aplikasi yang diverifikasi oleh F-Droid, Anda mendapatkan keuntungan dari unduhan yang andal dan aman.

Instalasi melalui F-Droid memberikan keuntungan berupa pembaruan aplikasi otomatis segera setelah dirilis. Selain itu, F-Droid menjamin bahwa aplikasi tersebut bebas dari komponen berbayar atau tertutup (proprietary) yang tidak diinginkan.

### Melalui GitHub (APK yang ditandatangani)

Jika Anda lebih suka menginstal aplikasi tanpa melalui toko aplikasi, Anda dapat mengunduh file APK resmi langsung dari halaman GitHub proyek tersebut. Pada repositori Aegis ([github.com/beemdevelopment/Aegis](https://github.com/beemdevelopment/Aegis)), buka bagian Releases tempat versi stable dipublikasikan.

- Unduh versi APK terbaru
- Sebelum menginstal APK, pastikan Anda telah mengizinkan instalasi aplikasi dari "sumber tidak dikenal" (unknown sources) di pengaturan Android Anda.
- APK yang disediakan di GitHub ditandatangani oleh pengembang dengan kunci yang sama seperti di F-Droid

Setelah instalasi manual, aplikasi akan berfungsi secara identik. Harap dicatat bahwa pembaruan tidak akan berjalan otomatis: Anda perlu memeriksa GitHub secara berkala untuk mengunduh versi terbaru.

### Google Play Store vs F-Droid

Aegis Authenticator tersedia di Google Play Store dan F-Droid, memberikan Anda pilihan metode instalasi:

**Google Play Store:**

- ✅ Pembaruan otomatis yang terintegrasi ke dalam sistem Android
- ✅ Instalasi yang sederhana dan familiar
- ✅ APK bertanda tangan yang sama seperti di saluran lain

**F-Droid (disarankan):**

- ✅ Toko opens soruce dan gratis
- ✅ Proses pembuatan aplikasi yang dapat direproduksi dan diverifikasi (reproducible builds).
- ✅ Tidak diperlukan layanan Google
- ✅ Menghormati filosofi free software

Pilihan di antara keduanya bergantung pada preferensi Anda terhadap ekosistem Google. Jika Anda menyukai kemudahan, Play Store adalah pilihan ideal. Jika Anda menginginkan pendekatan yang lebih menjaga privasi dan independen dari layanan Google, F-Droid adalah pilihan yang lebih baik.

## Konfigurasi pertama

Ketika Aegis diluncurkan untuk pertama kalinya, prosedur konfigurasi awal diusulkan untuk mengamankan kode 2FA Anda dengan aman:

![Configuration initiale Aegis](assets/fr/01.webp)

*Proses konfigurasi Aegis awal: layar selamat datang, pilihan keamanan, definisi kata sandi utama, dan finalisasi*

### Mengatur master password

Aegis pertama-tama akan meminta Anda untuk memilih kata sandi utama. Kata sandi ini akan digunakan untuk mengenkripsi semua token autentikasi Anda yang tersimpan di brankas. Kami sangat menyarankan agar Anda membuat kata sandi yang kuat dan unik yang hanya Anda yang tahu.

**⚠️ Peringatan:** Jangan lupa kata sandi ini - jika Anda lupa, kode 2FA terenkripsi Anda tidak akan dapat diakses (tidak ada pintu belakang). Aegis akan meminta Anda memasukkan kata sandi dua kali untuk konfirmasi.

### Mengaktifkan pembukaan kunci biometrik (opsional)

Jika perangkat Android Anda dilengkapi dengan pembaca sidik jari atau sensor biometrik lainnya, Aegis akan meminta Anda untuk mengaktifkan pembukaan kunci biometrik. Opsi ini opsional tetapi sangat praktis: memungkinkan Anda membuka kunci aplikasi dengan cepat menggunakan sidik jari atau wajah, daripada mengetikkan kata sandi setiap kali.

Perhatikan bahwa biometrik adalah kenyamanan tambahan: kata sandi utama Anda masih diperlukan jika biometrik diubah atau perangkat dihidupkan ulang.

### Temukan pengaturan aplikasi

Setelah Anda berada di dalam aplikasi (Interface utama awalnya kosong), kenalilah opsi konfigurasi yang tersedia. Akses pengaturan melalui menu drop-down di kanan atas layar (titik tiga vertikal), lalu pilih "Settings".

![Interface principale et paramètres](assets/fr/02.webp)

*Interface utama Aegis yang kosong di awal, akses ke menu parameter, dan ringkasan opsi yang tersedia.*

Menu pengaturan Aegis dikelompokkan beberapa bagian penting:

- **Appearance (Tampilan):** Kustomisasi tema (terang, gelap, AMOLED), bahasa, dan pengaturan visual lainnya.
- **Behavior (Perilaku):** Mengonfigurasi cara aplikasi merespons saat berinteraksi dengan daftar entri.
- **Icon packs:** Mengelola dan mengimpor paket ikon untuk mempersonalisasi tampilan akun Anda.
- **Security (Keamanan):** Pengaturan enkripsi, pembukaan kunci biometrik, penguncian otomatis, dan parameter keamanan lainnya.
- **Backups (Cadangan):** Mengonfigurasi pencadangan otomatis ke lokasi pilihan Anda.
- **Import & Export:** Mengimpor cadangan dari aplikasi autentikasi lain dan mengekspor brankas Aegis Anda secara manual.
- **Audit log:** Log detail dari semua peristiwa penting yang terjadi di aplikasi.

Pengelompokkan yang jelas ini memungkinkan Anda mengonfigurasi Aegis sesuai dengan preferensi dan kebutuhan keamanan Anda.

## Menambahkan akun 2FA

Setelah Aegis dikonfigurasi, mari lanjut ke hal esensial: menambahkan akun autentikasi dua faktor Anda. Prosesnya sederhana, dan Aegis menawarkan beberapa metode integrasi.

### Tiga metode penambahan yang tersedia

Dari Aegis Interface utama, tekan tombol **+** di kanan bawah untuk mengakses opsi tambah. Anda memiliki tiga pilihan:

- **Memindai kode QR**: Memindai secara langsung kode QR yang ditampilkan oleh layanan web
- **Memindai gambar**: Memindai kode QR dari gambar yang tersimpan di perangkat Anda
- **Masukkan secara manual**: Masukkan informasi akun 2FA secara manual

### Contoh praktis: mengkonfigurasi Bitwarden

Mari kita ambil contoh konkret aktivasi 2FA di Bitwarden untuk mengilustrasikan prosesnya:

![Exemple avec Bitwarden](assets/fr/04.webp)

*Contoh aktivasi 2FA di Bitwarden: Web Interface dengan opsi autentikasi dan rekomendasi Aegis*

- **Login dan mengakses pengaturan**: Masuk ke akun Bitwarden Anda dan akses pengaturan, tab "Security"
- **Bagian Penyedia**: Buka bagian "Providers" dan klik "Manage" di bagian "Authenticator app"

![Configuration 2FA avec QR code](assets/fr/05.webp)

*Proses lengkap penambahan akun: Kode QR yang ditampilkan layanan, kunci rahasia yang terlihat, dan kode verifikasi yang dimasukkan.*

- **Pindai kode QR**: Jendela popup terbuka dengan kode QR dan kunci rahasia
- Dalam **Aegis**: Gunakan "Scan QR Code" untuk menangkap informasi secara otomatis
- **Verifikasi**: Masukkan 6 digit kode yang dibuat oleh Aegis ke kolom "Verification code" di situs Bitwarden.
- **Aktivasi**: Klik "Turn On" untuk menyelesaikan aktivasi

### Menambahkan detail secara manual

Jika Anda lebih suka atau tidak dapat memindai kode QR, gunakan opsi "Enter manually". Formulir ini memungkinkan Anda untuk memasukkan :

![Ajout d'un compte 2FA](assets/fr/03.webp)

*Proses untuk menambahkan akun 2FA baru: Interface kosong, opsi tambah, formulir entri manual, dan akun berhasil ditambahkan*

- **Name** : Nama layanan (mis. Bitwarden, GitHub...)
- **Issuer** : Penerbit (sering kali identik dengan nama)
- **Group**: Opsional, untuk mengatur akun Anda berdasarkan kategori
- **Note**: Komentar pribadi di akun ini
- **Secret** : Kunci rahasia yang disediakan oleh layanan (disembunyikan secara default)
- **Advanced**: Parameter lanjutan (algoritme, periode, jumlah digit)

Setelah akun ditambahkan, akun tersebut akan muncul di daftar Anda dengan kode saat ini dan indikator waktu yang menunjukkan waktu yang tersisa sebelum pembaruan.

### Kompatibilitas universal

Aegis kompatibel dengan semua layanan yang menggunakan standar TOTP dan HOTP, termasuk hampir semua situs yang menawarkan 2FA: sosial media, bank, pengelola kata sandi, platform kripto, dll.

### Mengelola Daftar Akun

Setelah Anda menambahkan beberapa akun, Anda akan merasakan manfaat dari fitur pengelompokkan Aegis:

- **Pengurutan khusus:** Secara default, akun didaftarkan dalam urutan abjad, tetapi Anda dapat mengubah urutannya secara manual
- **Grup dan kategori:** Buat grup untuk memisahkan akun pribadi Anda dari akun bisnis, atau kelompokkan berdasarkan jenis layanan (perbankan, email, jejaring sosial, dll.)
- **Ikon yang disesuaikan:** Aegis mencoba untuk secara otomatis menetapkan ikon yang sesuai jika tersedia, jika tidak, Anda dapat memilih dari banyak ikon umum atau mengimpor gambar
- **Pencarian cepat:** Bilah pencarian di bagian atas memungkinkan Anda mengetikkan beberapa huruf untuk langsung menyaring entri yang cocok

- **Pengurutan khusus:** Secara default, akun disusun berdasarkan abjad, namun Anda dapat mengubah urutannya secara manual.
- **Grup dan Kategori:** Buat grup untuk memisahkan akun pribadi dari akun pekerjaan, atau kelompokkan berdasarkan jenis layanan (perbankan, email, media sosial, dll.).
- **Ikon Kustom:** Aegis mencoba menetapkan ikon yang sesuai secara otomatis. Jika tidak tersedia, Anda bisa memilih dari berbagai ikon umum atau mengimpor gambar sendiri.
- **Pencarian Cepat:** Kolom pencarian di bagian atas memungkinkan Anda mengetik beberapa huruf untuk menyaring entri yang cocok secara instan.

Dengan menyentuh sebuah entri, kode OTP akan ditampilkan dalam ukuran penuh (jika sebelumnya tersembunyi). Anda dapat menyalinnya ke clipboard dengan menekan lama—sangat praktis untuk menempelkan kode tersebut ke aplikasi yang ingin Anda akses.

## Keamanan dan pencadangan

Dengan keamanan sebagai inti dari Aegis, penting untuk memahami bagaimana kode 2FA Anda dilindungi, dan bagaimana memastikannya tetap ada jika terjadi masalah.

### Arsitektur keamanan

**Enkripsi Kuat:** Semua kode Anda disimpan dalam brankas terenkripsi menggunakan **algoritma AES-256 dalam mode GCM**, yang dikombinasikan dengan kata sandi utama (master password) Anda. Penurunan kunci (key derivation) menggunakan **scrypt**, yang menawarkan perlindungan lebih tinggi terhadap serangan brute-force.

**Pembukaan Kunci yang Aman:** Kata sandi utama diperlukan untuk mendekripsi data Anda. Fitur biometrik (opsional) menggunakan **Android Secure Keystore** dan TEE (*Trusted Execution Environment*) untuk melindungi kunci enkripsi.

**Izin Minimal:** Aegis beroperasi secara offline secara default, hanya memerlukan akses ke kamera (untuk pindai QR), biometrik, dan penggetar (vibrator). Tidak ada data yang dikumpulkan atau dibagikan.

Karena keamanan adalah inti dari Aegis, sangat penting untuk memahami bagaimana kode 2FA Anda dilindungi dan bagaimana memastikan data tersebut tetap ada jika terjadi masalah.

### Opsi pencadangan

Aegis menawarkan beberapa strategi pencadangan yang sesuai dengan kebutuhan keamanan dan kenyamanan yang berbeda:

![Configuration des sauvegardes](assets/fr/06.webp)

*Interface lengkap dengan akun yang ditambahkan, peringatan pencadangan, pengaturan pencadangan otomatis, dan strategi pencadangan*

**1. Pencadangan lokal otomatis**

- Konfigurasikan folder tujuan pilihan Anda
- Frekuensi yang dapat disesuaikan (setelah setiap perubahan, setiap hari, dll.)
- File terenkripsi yang dilindungi kata sandi (.aesvault)
- Kompatibel dengan penyimpanan cloud (Nextcloud, Dropbox, dll.)

![Sélection du dossier de sauvegarde](assets/fr/07.webp)

*Proses pemilihan folder cadangan: penjelajah file, folder tujuan, dan otorisasi akses*

**2. Pencadangan cloud Android**

- Integrasi opsional dengan sistem cadangan Android
- Hanya tersedia untuk brankas terenkripsi (keamanan terjaga)
- Pencadangan transparan dengan data Android lainnya
- Pemulihan otomatis saat pergantian perangkat

**3. Ekspor secara manual**

- Ekspor sesuai permintaan melalui **Pengaturan > Impor & Ekspor**
- Pilihan format terenkripsi (disarankan) atau format yang jelas
- Berguna untuk migrasi atau pencadangan sesekali

### Praktik-praktik keamanan yang baik

- Simpan beberapa versi **cadangan** untuk mencegah kerusakan
- **Uji** cadangan Anda secara teratur dengan mencoba memulihkannya
- Simpan kode pemulihan yang disediakan oleh layanan Anda secara terpisah
- Kata sandi utama **Anda** masih diperlukan bahkan dengan cadangan cloud
- **Amankan kata sandi utama Anda**: gunakan kata sandi yang unik dan kuat yang disimpan dalam pengelola kata sandi
- Selalu perbarui **aplikasi Anda** dengan patch keamanan terbaru
- Aktifkan **penguncian otomatis** dalam pengaturan untuk mengamankan akses ke aplikasi
- Nonaktifkan **tangkapan layar** (opsi default) untuk mencegah kode Anda disadap
- **Gunakan biometrik dengan bijak**: lebih memilih kata sandi untuk akses penting

## Perbandingan dengan aplikasi lain

Bagaimana Aegis dibandingkan dengan aplikasi autentikasi populer lainnya?

### Aegis vs Google Authenticator

**Aegis :**

- ✅ Open source dan dapat diaudit
- ✅ Cadangan terenkripsi lokal
- ✅ Organisasi lanjutan (grup, ikon, pencarian)
- ✅ Tidak ada pengumpulan data
- ❌ Hanya untuk Android

**Pengesahan Google :**

- ✅ Tersedia di Android dan iOS
- ✅ Sinkronisasi cloud (sejak tahun 2023)
- ❌ Source code tertutup
- ❌ Fungsionalitas terbatas
- ❌ Potensi pengumpulan data Google

### Aegis vs Authy

**Aegis :**

- ✅ Open source 
- ✅ Tidak diperlukan akun
- ✅ Ekspor kode dimungkinkan
- ✅ Kontrol data total
- ❌ Tidak ada sinkronisasi multi-perangkat secara langsung

**Authy :**

- ✅ Sinkronisasi multi-perangkat
- ✅ Tersedia di Android dan iOS
- ❌ Source code tertutup
- ❌ Memerlukan nomor telepon
- ❌ Tidak dapat mengekspor kode
- ❌ Aplikasi desktop dihapus pada bulan Maret 2024

Aegis adalah pilihan yang sangat unggul bagi pengguna Android yang mengutamakan transparansi, keamanan lokal, dan kendali penuh atas data mereka. Alternatif lain seperti Authy mungkin lebih cocok jika Anda benar-benar membutuhkan sinkronisasi otomatis antar-perangkat (multi-device synchronization).

## Kesimpulan

Aegis Authenticator adalah solusi luar biasa bagi mereka yang mencari aplikasi 2FA yang aman, transparan, dan ramah privasi. Pendekatan open-source yang digunakannya, dikombinasikan dengan enkripsi yang kuat dan interface yang rapi, menjadikannya pilihan utama untuk mengamankan akun online Anda.

Meskipun terbatas pada Android dan tidak memiliki sinkronisasi cloud bawaan, Aegis menutupi keterbatasan tersebut dengan filosofi "privacy by design" dan kendali data total. Bagi pengguna yang peduli dengan privasi digital mereka, Aegis menawarkan alternatif yang kredibel dan kuat dibandingkan solusi berbayar (proprietary) yang mendominasi pasar.

Keamanan akun online Anda tidak harus bergantung pada niat baik perusahaan komersial. Dengan Aegis, Anda tetap memegang kendali atas kode autentikasi Anda di dalam brankas digital yang kuncinya hanya Anda yang pegang.

## Sumber daya

### Situs web resmi

- **Situs web resmi**: [getaegis.app](https://getaegis.app/) - Presentasi dan pengunduhan aplikasi
- **Source code**: [github.com/beemdevelopment/Aegis](https://github.com/beemdevelopment/Aegis) - Repositori resmi GitHub
- **F-Droid**: [f-droid.org/packages/com.beemdevelopment.aegis](https://f-droid.org/packages/com.beemdevelopment.aegis/) - Instalasi melalui toko gratis

### Dokumentasi teknis

- **Dokumentasi Vault**: [Desain Vault](https://github.com/beemdevelopment/Aegis/blob/master/docs/vault.md) - Deskripsi teknis enkripsi dan arsitektur yang aman
- **Pertanyaan Umum Resmi**: [getaegis.app/#faq](https://getaegis.app/#faq) - Jawaban atas pertanyaan yang sering diajukan
- **Wiki proyek**: [github.com/beemdevelopment/Aegis/wiki](https://github.com/beemdevelopment/Aegis/wiki) - Dokumentasi pengguna lengkap
