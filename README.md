Struktur HTML (Semantic):
Saya menggunakan tag HTML5 semantik seperti <header>, <main>, <section>, <footer>, dan <nav> untuk membantu mesin pencari memahami struktur halaman dan untuk aksesibilitas yang lebih baik.
Setiap bagian memiliki id yang sesuai (#home, #products, #compliance) agar navigasi berfungsi dengan lancar.
Desain & Vibe Visual (CSS):
CSS Variables: Warna utama (--forest-green, --charcoal-black) disimpan di :root. Ini memudahkan Anda jika ingin mengubah skema warna di masa depan.
Font: Menggunakan Montserrat dari Google Fonts untuk memberikan kesan modern dan profesional.
Layout: Menggunakan Flexbox dan Grid untuk membuat tata letak yang rapi dan responsif.
Responsif: Terdapat @media query yang menyesuaikan tampilan untuk layar ponsel, seperti menumpuk navigasi dan detail produk.
Toggle Bahasa (JavaScript):
Teks yang perlu diterjemahkan memiliki atribut data-translate.
Fungsi switchLanguage() akan mengganti nilai currentLanguage dan memperbarui teks di semua elemen yang sesuai berdasarkan objek translations.
Tab Produk (JavaScript):
Fungsi showTab() dijalankan saat tombol tab diklik. Fungsi ini menyembunyikan konten tab lain dan menampilkan konten tab yang dipilih, serta mengubah kelas active pada tombol untuk indikasi visual.
Kalkulator Konversi Harga (Fitur Utama):
API Kurs: Saat halaman dimuat, fungsi fetchExchangeRate() dipanggil untuk mengambil data kurs IDR ke USD secara real-time dari exchangerate-api.com. Jika gagal, akan menggunakan nilai fallback (kurs cadangan) agar kalkulator tetap berfungsi.
Perhitungan Real-time: Fungsi calculatePrice(productKey) dipanggil setiap kali Anda mengetik di input field. Fungsi ini langsung menghitung dan menampilkan hasil konversi ke USD.
Integrasi WhatsApp: Fungsi sendToWhatsApp(productKey) adalah "senjata" utamanya.
Ia mengambil nilai dari input dan hasil perhitungan.
Ia menggunakan template pesan (waMessageTemplate) yang sudah disesuaikan dengan bahasa yang aktif.
Ia mengganti placeholder (%PRODUCT%, %TOTAL_USD%) dengan data yang sesuai.
Terakhir, ia membuka aplikasi WhatsApp (Web/Desktop) dengan URL yang sudah berisi pesan yang lengkap dan siap dikirim.
Tombol WhatsApp Melayang (Floating Button):
Tombol ini selalu terlihat di pojok kanan bawah menggunakan position: fixed. Ini memberikan akses cepat bagi pengunjung untuk menghubungi Anda, bahkan jika mereka sedang scroll di bagian mana pun.
Kustomisasi:
Nomor WhatsApp: Ganti 6281234567890 di dua tempat (dalam fungsi sendToWhatsApp dan di floating-wa) dengan nomor WhatsApp bisnis Anda (gunakan format kode negara).
Gambar: Ganti URL gambar placeholder (https://via.placeholder.com/... dan URL Pexels) dengan foto asli produk, gudang, dan tim Anda.
Spesifikasi Produk: Edit tabel spesifikasi sesuai data produk Anda yang sebenarnya.
API Kurs: Untuk produksi, pertimbangkan untuk menggunakan API berbayar yang lebih stabil atau cache hasilnya untuk beberapa jam agar tidak membebani server.
Desain ini akan menampilkan:
Animasi Scroll yang Halus: Elemen-elemen akan muncul dengan animasi yang menarik saat pengguna scroll.
Tipografi yang Berlapis: Menggunakan font yang berbeda untuk heading dan body text untuk menciptakan hierarki visual yang kuat.
Layout Asimetris & Whitespace: Penggunaan ruang kosong yang maksimal dan tata letak yang tidak monoton untuk memberikan kesan mewah dan modern.
Interaksi Mikro: Efek hover yang halus pada tombol dan kartu produk.
Kalkulator Harga yang Redesigned: Tampilan kalkulator yang lebih futuristik dan terintegrasi.
Video Hero Section: Menggunakan video background untuk kesan sinematik yang maksimal (saya akan menggunakan placeholder, Anda bisa menggantinya dengan video asli).
