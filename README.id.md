<p align="center">
  <a href="https://mail.chatgpt.org.uk/">
    <img src="https://mail.chatgpt.org.uk/logo.svg" width="88" height="88" alt="Logo email sementara GPTMail">
  </a>
</p>

<h1 align="center">GPTMail — Email Sementara Gratis</h1>

<p align="center">
  Buat alamat email sekali pakai dalam hitungan detik untuk menerima kode verifikasi, tautan konfirmasi, dan email pengujian tanpa membanjiri kotak masuk utama.
</p>

<p align="center">
  <a href="https://mail.chatgpt.org.uk/"><strong>Buka GPTMail</strong></a> ·
  <a href="https://chromewebstore.google.com/detail/eplebonhkjiahfnoaiifngokamaipeoo">Ekstensi Chrome</a> ·
  <a href="https://mail.chatgpt.org.uk/help">Pusat bantuan</a> ·
  <a href="https://mail.chatgpt.org.uk/api">API developer</a>
</p>

<p align="center">
  <a href="README.md">English</a> ·
  <a href="README.zh-CN.md">简体中文</a> ·
  <strong>Bahasa Indonesia</strong>
</p>

[![Tampilan email sementara gratis GPTMail](https://mail.chatgpt.org.uk/og.png)](https://mail.chatgpt.org.uk/)

## Kotak masuk sementara yang langsung siap dipakai

GPTMail adalah layanan email sementara gratis untuk pendaftaran singkat, penerimaan kode OTP, konfirmasi akun, pengujian perangkat lunak, dan situasi ketika Anda tidak ingin memberikan alamat email permanen. Saat situs dibuka, sebuah alamat sudah tersedia tanpa proses pendaftaran untuk kotak masuk publik.

Email disimpan selama **24 jam**. Waktu tersebut cukup untuk sebagian besar proses verifikasi, tetapi tetap membatasi jejak pesan dan mengurangi risiko menerima promosi selama bertahun-tahun hanya karena satu kali mendaftar.

## Fitur utama

| Fitur | Kegunaan |
| --- | --- |
| Alamat email instan | Langsung menerima email tanpa membuat akun |
| Ekstraksi kode verifikasi | Membantu menemukan kode sekali pakai dan tautan konfirmasi |
| Pilihan domain aktif | Beralih ke domain lain jika alamat pertama ditolak |
| Awalan alamat khusus | Membuat alamat yang mudah dikenali untuk suatu pengujian |
| Domain publik dan privat | Memilih kemudahan kotak masuk publik atau perlindungan kata sandi |
| Gunakan domain sendiri | Menghubungkan domain yang Anda kendalikan ke GPTMail |
| Ekstensi Chrome | Membuat alamat dan memeriksa email dari browser |
| API developer | Mengotomatiskan alur QA dan pengujian email |
| Notifikasi Telegram | Mendapatkan pemberitahuan saat pesan baru tiba |
| Tampilan responsif | Nyaman digunakan di ponsel maupun desktop |

## Cara menggunakan email sementara

1. Buka **[mail.chatgpt.org.uk](https://mail.chatgpt.org.uk/)**.
2. Gunakan alamat yang sudah dibuat atau tekan **Random** untuk memperoleh alamat baru.
3. Masukkan alamat tersebut pada formulir pendaftaran, uji coba, unduhan, atau pengujian.
4. Kembali ke GPTMail dan tunggu pesan muncul di kotak masuk.
5. Buka pesan untuk membaca kode verifikasi atau tautan konfirmasi.

Jika sebuah situs tidak menerima domain yang dipilih, gunakan pemilih domain untuk membuat alamat dengan akhiran lain. Ketersediaan domain dapat berubah karena setiap domain bergantung pada konfigurasi DNS dan MX yang valid.

## Ekstensi Chrome GPTMail

**[Ekstensi GPTMail untuk Chrome](https://chromewebstore.google.com/detail/eplebonhkjiahfnoaiifngokamaipeoo)** memudahkan penggunaan email sementara tanpa bolak-balik tab. Ekstensi ini dapat:

- membuat dan mengganti alamat sementara;
- menampilkan pesan yang belum dibaca dari toolbar atau panel samping;
- memberi notifikasi saat email baru tiba;
- menyarankan alamat aktif pada kolom email setelah izin opsional diberikan;
- mengotorisasi setiap instalasi browser secara terpisah tanpa menanam API key bersama.

Situs web tetap dapat digunakan sepenuhnya tanpa memasang ekstensi.

## Perbedaan kotak masuk publik dan privat

**Kotak masuk publik bukan tempat untuk informasi rahasia.** Siapa pun yang mengetahui alamat lengkap mungkin dapat membukanya. Jangan gunakan email sementara publik untuk perbankan, dokumen identitas, informasi kesehatan, pemulihan akun, akun jangka panjang, atau percakapan pribadi.

Jika memiliki domain sendiri, Anda dapat memilih:

- **Domain khusus publik:** alamat pada domain berfungsi seperti kotak masuk publik GPTMail lainnya;
- **Domain khusus privat:** kotak masuk dilindungi kata sandi yang ditetapkan pemilik domain;
- **Konfigurasi DNS berbantuan Cloudflare:** pemilik domain dapat memakai proses otorisasi terbatas untuk menambahkan MX yang diperlukan dan mengurangi kesalahan konfigurasi manual.

## Untuk developer dan tim QA

Kotak masuk sekali pakai berguna ketika pengujian harus menerima email sungguhan, misalnya:

- pengujian pendaftaran dan verifikasi email;
- magic link dan login tanpa kata sandi;
- notifikasi dari lingkungan staging;
- alamat unik untuk pengujian end-to-end;
- pemeriksaan pengiriman email selama pengembangan;
- data uji yang tidak seharusnya masuk ke email karyawan.

GPTMail menyediakan antarmuka web dan API HTTP. Kirim API key melalui header permintaan, jangan menaruh kredensial di URL atau log, dan pertimbangkan adanya jeda normal dalam pengiriman email. Lihat **[dokumentasi API GPTMail](https://mail.chatgpt.org.uk/api)** untuk rincian terbaru.

## Pertanyaan umum

### Apa itu email sementara?

Email sementara adalah alamat jangka pendek untuk menerima pesan tanpa membagikan email pribadi atau kantor. Istilah lain yang sering digunakan adalah disposable email, temp mail, email sekali pakai, dan kotak masuk sementara.

### Apakah GPTMail dapat menerima kode OTP atau verifikasi?

Ya. GPTMail menerima email biasa pada domain yang didukung dan mencoba menyoroti kode serta tautan konfirmasi yang umum. Fitur ekstraksi hanya membantu; periksa isi pesan lengkap untuk tindakan penting.

### Apakah harus mendaftar?

Tidak ada pendaftaran untuk kotak masuk publik. Kotak masuk pada domain privat memerlukan kata sandi yang dibuat pemilik domain.

### Berapa lama email disimpan?

Saat ini email disimpan selama 24 jam. Pesan dapat hilang lebih cepat jika dihapus atau kotak masuk dikosongkan oleh pengguna.

### Apakah kotak masuk publik bersifat pribadi?

Tidak. Gunakan hanya untuk pesan singkat dan berisiko rendah. Jangan mengirim atau menerima data sensitif melalui kotak masuk publik.

### Apakah GPTMail membuat akun Gmail atau Outlook?

Tidak. GPTMail menyediakan kotak masuk sementara pada domain yang didukung dan tidak membuat akun permanen di layanan pihak ketiga.

## Penggunaan yang bertanggung jawab

Gunakan GPTMail hanya jika layanan tujuan mengizinkan alamat sementara. Jangan menggunakannya untuk penipuan, pelecehan, spam, melewati perlindungan platform, atau menerima informasi sensitif. Situs pihak ketiga dapat menolak alamat sekali pakai, dan GPTMail tidak dapat menjamin setiap domain selalu diterima.

## Pelajari lebih lanjut

- [Cara kerja email sementara](docs/how-temporary-email-works.md)
- [Domain khusus dan kotak masuk privat](docs/custom-domains-and-private-inboxes.md)
- [Alur pengujian dan API](docs/testing-and-api-workflows.md)
- [Pusat bantuan GPTMail](https://mail.chatgpt.org.uk/help)
- [Ketentuan dan privasi](https://mail.chatgpt.org.uk/terms)
- [Pembaruan produk dan panduan](https://mail.chatgpt.org.uk/blog)

---

GPTMail tidak berafiliasi dengan OpenAI, ChatGPT, Google, Microsoft, Telegram, atau layanan pihak ketiga lain yang disebutkan. Nama produk adalah milik pemegang hak masing-masing.