# 🎙️ AudioSync Studio

**Sinkronisasi voice-over, foto, dan video untuk content creator.**

AudioSync Studio adalah aplikasi lokal untuk Windows yang membantu menyusun scene visual sesuai durasi narasi. Proyek ini ditujukan untuk workflow konten YouTube, Reels, dan video edukasi: dari script dan voice-over, sampai ekspor video yang dapat dilanjutkan editing-nya di CapCut.

> **Status:** v2.1.0-rc.1 (Beta / versi uji). Fitur, kompatibilitas, dan kebutuhan instalasi dapat berubah. Sebagian proses AI memakai model yang harus tersedia atau diunduh secara terpisah.

## ⬇️ Download

**[Download AudioSync Studio untuk Windows (GitHub Releases)](https://github.com/mhdariee/AudioSync-Studio/releases/tag/v2.1.0-rc.1)**

Pada bagian **Assets**, pilih **`AudioSyncStudio-2.1.0-rc.1-Windows.zip`**. Jangan memilih **Source code (zip)** jika tujuanmu menginstal aplikasi.

## ✨ Fitur

- **Voice-over bahasa Inggris:** generate narasi menggunakan Kokoro TTS lokal, jika model dan dependensi sudah terpasang.
- **Impor narasi Indonesia:** gunakan rekaman WAV/MP3 milikmu sendiri. **Generate AI voice bahasa Indonesia belum terverifikasi tersedia pada rilis ini.**
- **Sinkronisasi scene:** sesuaikan waktu tampil foto/video dengan narasi.
- **Impor gambar/video:** dukungan JPG, PNG, WebP, dan MP4 sesuai build.
- **AI-assisted scene matching:** bantuan mencocokkan gambar dengan isi script, jika komponen model lokal telah tersedia. Hasil perlu ditinjau karena AI bisa keliru.
- **Subtitle opsional:** tanpa subtitle, file terpisah, atau subtitle permanen sesuai mode yang tersedia.
- **Ekspor MP4 dan paket CapCut:** untuk melanjutkan editing subtitle, transisi, musik, dan efek.

## 💻 Persyaratan

- **Sistem operasi:** Windows 11. Kompatibilitas Windows 10 belum dikonfirmasi.
- **RAM:** disarankan 16 GB agar pengolahan AI dan media lebih leluasa.
- **GPU:** NVIDIA RTX membantu sebagian pemrosesan, tetapi beberapa fitur dapat berjalan dengan CPU. Kinerja bergantung pada model dan perangkat.
- **Penyimpanan:** sediakan ruang kosong tambahan untuk Python/runtime, FFmpeg, model AI, cache, dan hasil video. Ukuran ZIP rilis **bukan** ukuran total pemasangan.
- **Internet:** mungkin diperlukan pada instalasi pertama untuk mengunduh dependensi dan model. Fitur lokal yang telah lengkap dapat bekerja tanpa langganan TTS, tetapi operasi offline penuh perlu diuji pada masing-masing instalasi.

> Persyaratan di atas merupakan rekomendasi awal, **belum merupakan minimum resmi yang teruji pada berbagai komputer**.

## 🛠️ Cara instalasi (Windows)

1. Buka halaman **Download** di atas.
2. Pada **Assets**, download `AudioSyncStudio-2.1.0-rc.1-Windows.zip`.
3. Klik kanan ZIP → **Extract All** / **Ekstrak Semua**.
4. Buka folder hasil ekstrak dan baca dokumen instalasi yang disertakan, jika ada.
5. **Jika** terdapat `AudioSyncStudio-Setup.exe`, jalankan installer itu dan ikuti petunjuknya. Jangan menjalankan file executable yang tidak kamu percayai.
6. **Jika installer tidak ada**, paket ini belum terbukti bisa dipasang sekali klik. Laporkan isi ZIP melalui GitHub Issues agar pembuat aplikasi bisa memberikan panduan yang sesuai; jangan menganggap file *Source code (zip)* sebagai installer.
7. Setelah terpasang, buka **AudioSync Studio** dari shortcut Desktop atau launcher yang disediakan.

**Catatan:** Paket installer belum diverifikasi di sini pada komputer Windows yang bersih. Windows SmartScreen bisa menampilkan peringatan untuk aplikasi baru yang belum ditandatangani; pastikan file berasal dari halaman rilis resmi, periksa isi paket, dan jangan menonaktifkan perlindungan sistem secara membabi buta.

## 🎬 Cara menggunakan

1. **Script** — Masukkan atau impor naskah. Usahakan satu kalimat/visual per scene bila menggunakan pencocokan berurutan.
2. **Voice** — Pilih bahasa. Untuk English, generate Kokoro voice; untuk Indonesia, impor audio sesuai petunjuk aplikasi.
3. **Scenes** — Impor gambar dan klip video. Jika nama file acak, gunakan **AI Scene Matching** bila tersedia, lalu **periksa urutan secara manual**. Jangan mengandalkan tebakan AI tanpa review.
4. **Timeline** — Periksa waktu mulai, akhir, dan durasi setiap scene. Sesuaikan jika ada kesalahan.
5. **Subtitles** — Pilih mode tanpa subtitle, subtitle terpisah, atau subtitle permanen.
6. **Export** — Ekspor MP4 atau paket **Export for CapCut**.

### Mengedit di CapCut

Pada paket CapCut, gunakan klip scene berurutan serta `narration.wav` mulai detik 00:00. Jika tersedia, impor `subtitles.srt` secara terpisah. **Jangan mencampur audio dari `final_preview.mp4` dengan `narration.wav` sekaligus** karena dapat menghasilkan suara ganda. Periksa ulang sinkronisasi setelah menambah transisi yang mengubah durasi klip.

## ❓ Masalah yang sering terjadi

| Kendala | Yang bisa dicoba |
|---|---|
| Aplikasi tidak terbuka | Periksa panduan instalasi, launcher, dan log aplikasi. Laporkan pesan error yang tampil. |
| Voice English gagal dibuat | Periksa apakah model Kokoro dan dependensinya sudah diunduh/terpasang; cek koneksi saat setup awal. |
| Bahasa Indonesia hanya bisa impor audio | Ini adalah keterbatasan versi saat ini; jangan menganggap generate TTS Indonesia sudah aktif. |
| Gambar acak dianggap `Invalid` / `Missing` | Mode impor bernomor memerlukan nama seperti `scene_001.png`. Coba **AI Scene Matching** jika ada dan konfirmasi hasilnya. |
| Video tidak sinkron setelah masuk CapCut | Pastikan urutan scene, awal track narasi di 00:00, dan perubahan durasi akibat transisi. |
| Render terasa lambat | Coba proyek kecil terlebih dahulu, tutup aplikasi berat lain, dan cek ruang disk serta RAM. |

Untuk melaporkan bug: **[GitHub Issues](https://github.com/mhdariee/AudioSync-Studio/issues)**. Sertakan versi Windows, spesifikasi komputer, langkah memunculkan error, dan screenshot **tanpa informasi pribadi**.

## 💰 Apakah gratis?

Aplikasi ini dibagikan sebagai **tool gratis** untuk digunakan secara lokal. Pemrosesan lokal tidak memerlukan langganan ChatGPT/Codex untuk sekadar menjalankan aplikasi yang telah terpasang. Namun, unduhan model, penggunaan layanan pihak ketiga (jika kamu menambahkannya), koneksi internet, dan lisensi model memiliki ketentuan masing-masing. **Gratis dipakai tidak otomatis berarti seluruh komponen boleh didistribusikan ulang atau dipakai secara komersial.** Periksa berkas lisensi/notices pada paket.

## 🔒 Privasi dan keamanan

- Hindari mengunggah data pribadi, API key, token, atau rekaman sensitif ke laporan bug publik.
- Periksa ZIP rilis sebelum memasangnya; file pada GitHub Releases berbeda dari arsip **Source code** otomatis.
- Bila membagikan ulang, pastikan hak redistribusi kode, FFmpeg, suara/model AI, dan aset visual terpenuhi.

## 🤝 Feedback

Masukan, laporan bug, dan saran fitur bisa disampaikan lewat **[Issues](https://github.com/mhdariee/AudioSync-Studio/issues)**.

Dibuat untuk membantu kreator lebih fokus pada cerita, bukan menggeser ratusan scene satu per satu.
