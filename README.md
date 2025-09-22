README – Profil Instagram (Bootstrap & Tailwind)

Deskripsi
Membuat halaman profil Instagram versi sederhana dengan dua pendekatan:
1. Bootstrap 5 – memanfaatkan komponen bawaan dan grid system.
2. Tailwind CSS – menggunakan utility-first classes untuk membangun layout secara responsif.

Tujuan utama:
- Membuat halaman profil Instagram yang responsif (mobile-first).
- Struktur utama: Header Profil, Bio, Feed (minimal 12 gambar), Footer.
- Membandingkan pengalaman implementasi Bootstrap vs Tailwind.

---

Pertanyaan Reflektif

1. Keputusan grid-cols/gap di tiap breakpoint (Tailwind) & grid system (Bootstrap)
- Tailwind:  
  Menggunakan `grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4` agar layout mobile, tablet, desktop menyesuaikan. Gap diatur dengan `gap-2` supaya feed terlihat rapat seperti Instagram.
- Bootstrap:
  Menggunakan grid system bawaan (`col-6 col-md-4 col-lg-3`) sehingga otomatis responsif sesuai breakpoint. Gap antar foto bisa diatur dengan `g-2`.

Alasan:
Instagram pada mobile menampilkan 1 kolom, tablet biasanya 2–3 kolom, dan desktop 3–4 kolom. Jadi penentuan ini logis untuk kenyamanan pengguna.

---

2. Pemanfaatan utility responsive (Tailwind) & utility Bootstrap
- Tailwind: 
  Menggunakan class responsive seperti `sm:`, `md:`, `lg:` untuk mengubah jumlah kolom, ukuran tombol, dan alignment.  
  Contoh: tombol Follow/Edit berubah ukuran di breakpoint tertentu.
- Bootstrap:  
  Memanfaatkan utility responsive seperti `d-md-flex`, `text-center text-md-start`, atau grid responsive. Komponen bawaan mempermudah tanpa harus bikin class baru.

Kesimpulan:  
Keduanya membantu menyelesaikan masalah layout di layar kecil, hanya saja pendekatan berbeda: Tailwind lebih granular, Bootstrap lebih siap pakai.

---

3. Trade-off: banyak utility class vs component CSS
- Tailwind: 
   Cepat styling tanpa bikin file CSS tambahan.  
   HTML bisa jadi panjang karena penuh class.  
- Bootstrap:
   Kode lebih ringkas jika pakai komponen siap pakai (misal card, navbar).  
   Kadang perlu override CSS kalau ingin style khusus.

**Trade-off:**  
Tailwind memberi fleksibilitas penuh tapi verbose, sedangkan Bootstrap lebih cepat untuk standar UI tapi kurang fleksibel.
