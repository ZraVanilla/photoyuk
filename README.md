📸 Photo Yuk
Deskripsi
Photo yuk adalah sebuah aplikasi web sederhana yang memungkinkan pengguna untuk:

Mengakses kamera secara langsung.

Mengambil foto dengan template frame lucu.

Mengunduh hasil foto secara instan.

Aplikasi ini cocok untuk keperluan event kecil, booth online, ataupun sekadar hiburan.

🚀 Fitur
Mengakses kamera perangkat (desktop & mobile).

Template frame unik yang dapat diubah sesuai kebutuhan.

Tombol untuk mengambil foto dan mengunduh hasilnya.

Tampilan responsif dan modern.

Kamera non-mirror (hasil foto tidak terbalik).

🛠️ Teknologi yang Digunakan
HTML5: Struktur halaman.

CSS3: Styling dan layout modern.

JavaScript: Akses kamera, capture, dan download foto.

Web APIs: getUserMedia untuk mengakses kamera.

💡 Cara Menjalankan
Clone repository:

Buka file index.html langsung di browser.

Izinkan akses kamera saat diminta.

🤖 Penjelasan Dukungan AI
Dalam proses pengembangan, saya menggunakan bantuan AI IBM Granite untuk:

Membantu merancang layout halaman.

Memberikan referensi styling modern.

Menyediakan saran perbaikan pada alur capture foto.

AI digunakan hanya pada fase pengembangan, tidak disertakan dalam produk akhir.

📂 Deployment
Project ini dapat dideploy menggunakan:

Netlify

📸 Screenshot

![image](https://github.com/user-attachments/assets/402f8e00-0c90-4086-a2a9-150ad15f0037)
![image](https://github.com/user-attachments/assets/2ff535c5-1977-4bc0-b8ca-48a718d3b16d)
![image](https://github.com/user-attachments/assets/3f5c094f-9996-4913-a8cc-a04bc6c8cd02)


Link demo [(kalau sudah dideploy).](https://preeminent-donut-330bb3.netlify.app/)


## Masalah
**Masalah**: Tombol restart kamera sering stuck di "Inisialisasi Kamera..."
           : Masalah Resposive pada tampilan ukuran kamera dan bentuk frame di beberapa device, tetapi tidak merubah hasil

**Penyebab**:
1. Elemen video tidak dibersihkan dengan benar saat restart
2. Tidak ada timeout untuk mencegah stuck
3. Penanganan error yang kurang baik
4. Konflik antara elemen canvas dan video

**Solusi yang Diimplementasikan**:

1. **Perbaikan Fungsi Restart**:
   - Membersihkan semua elemen video dan canvas yang ada
   - Reset semua variabel state
   - Menambahkan timeout untuk mencegah stuck

2. **Fungsi Force Restart**:
   - Restart yang lebih agresif
   - Membersihkan semua media stream
   - Reset semua UI elements

3. **Timeout Mechanism**:
   - Timeout 10 detik untuk inisialisasi utama
   - Timeout 8 detik untuk fallback
   - Auto-clear timeout saat berhasil

4. **Debug Tools**:
   - Tombol debug untuk troubleshooting
   - Logging yang lebih detail
   - Status monitoring

## Cara Menggunakan

1. **Restart Normal**: Gunakan tombol "🔄 Restart Kamera" untuk restart biasa
2. **Force Restart**: Gunakan tombol "🚨 Force Restart" jika restart normal stuck
3. **Debug**: Gunakan tombol "🐛 Debug" untuk melihat status kamera di console

## Troubleshooting

### Jika Kamera Stuck di Inisialisasi:

1. **Coba Force Restart**: Klik tombol "🚨 Force Restart"
2. **Refresh Browser**: Reload halaman
3. **Cek Izin Kamera**: Pastikan browser mendapat izin akses kamera
4. **Cek Console**: Tekan F12 dan lihat error di console
5. **Gunakan Debug**: Klik tombol debug untuk info detail

### Tips Performa:

- Gunakan CSS Mode untuk performa lebih baik
- Hindari efek GLFX jika device lambat
- Gunakan tombol "🛑 Stop Efek" jika aplikasi freeze

## Teknologi

- HTML5 Canvas
- WebRTC (getUserMedia)
- GLFX.js untuk efek advanced
- CSS3 untuk animasi dan efek
- js untuk animasi button dan lainnya

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge

Pastikan browser mendukung WebRTC dan getUserMedia API.

## Fitur

- 📸 Ambil foto dengan kamera
- 🖼️ Pilih frame foto (6 frame custom)
- 🎨 Filter warna dan efek lensa
- ✨ Efek khusus (pulse, shake, glow)
- 💕 Efek Love dengan animasi romantis
- 🌹 Mode Love dengan berbagai tema
- 🎉 Love Celebration dengan efek spektakuler
- 💾 Download foto hasil
- 🎯 Mode bersih (clean mode) untuk interface minimalis
- ⌨️ Keyboard shortcuts untuk kemudahan penggunaan
- 🔧 Kontrol yang dapat disembunyikan untuk pengalaman yang lebih baik

## Frame Options 🖼️
ada pilihan 6 frame yang tersedia

### Opsi Lain:
- **Tanpa Frame**: Ambil foto tanpa frame apapun

### Cara Menambahkan Frame:
1. Siapkan gambar frame dengan format PNG
2. Simpan di folder `assets/` dengan nama `frame1.png`, `frame2.png`, dst
3. Pastikan ukuran frame sesuai dengan video (640x480px)
4. Frame akan otomatis muncul di selector

## Efek Love 💕

### Efek Khusus Love:
- **💕 Love**: Efek cinta dengan animasi lembut dan floating hearts
- **💖 Hearts**: Efek hati dengan warna-warna romantis
- **🌹 Romantic**: Efek romantis dengan filter dreamy
- **✨ Sparkle**: Efek berkilau dengan animasi sparkle

### Mode Love:
- **🍯 Sweet Love**: Efek cinta manis dengan warna pink lembut
- **🔥 Passionate**: Efek cinta bergairah dengan warna merah intens
- **💭 Dreamy**: Efek cinta impian dengan blur dan warna lembut
- **✨ Magical**: Efek cinta magis dengan warna-warna ajaib

### Love Celebration 🎉:
- **💝 Love Celebration**: Efek perayaan cinta dengan multiple floating elements
- **🛑 Stop**: Hentikan semua efek celebration

## Kontrol Interface

### Tombol Utama:
- **📸 Foto**: Ambil foto dengan frame
- **📸 Tanpa Frame**: Ambil foto tanpa frame
- **💾 Download**: Download foto hasil
- **🔄 Ulang**: Ambil foto ulang

### Tombol Kontrol Kamera:
- **🔄 Restart**: Restart kamera normal
- **🚨 Force**: Force restart kamera (untuk kasus stuck)
- **🐛 Debug**: Lihat status kamera di console

### Tombol Pengaturan:
- **⚙️**: Tampilkan/sembunyikan kontrol advanced
- **🎯**: Mode bersih (hanya tombol utama)

## Keyboard Shortcuts

- **Spacebar**: Ambil foto
- **H**: Sembunyikan/tampilkan kontrol kamera
- **Escape**: Ambil ulang foto (jika sudah ada foto)

## Gesture Controls

- **Double-click** pada area kamera: Sembunyikan/tampilkan kontrol
