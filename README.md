![alt text](https://j.top4top.io/p_3555iolt81.png?raw=true)

🔍 Apa itu IP Live Checker?
Sederhananya:
❓ "IP ini masih aktif nggak sih?"
💡 IP Live Checker: "Bentar, gue cekin... ✅ Hidup!" atau ❌ "Mati!"

Cara kerja kode ini, step-by-step, dengan rasa:

Warming up 🔥

Kode ini mulai dengan import modul penting seperti socket untuk koneksi jaringan, threading untuk bikin proses cek bisa jalan paralel, dan beberapa modul untuk warna dan manipulasi file.

Mengecat terminal biar keren 🎨

Ada kelas Colors buat bikin output di terminal lebih hidup. Jadi, ketika IP atau port berhasil atau gagal dicek, tampilannya warna-warni sesuai statusnya.

Clear layar, tampilkan banner 🧹🖥️

Sebelum mulai, layar dibersihkan supaya hasilnya nggak berantakan, terus banner keren muncul yang menunjukkan siapa pembuatnya.

Minta input dari pengguna 🖥️⌨️

1. Minta file berisi daftar IP. Kalau file nggak ada, program bakal ngasih tahu errornya.
2. Minta daftar port yang ingin dicek, misalnya 80,443,8080.
3. Minta jumlah thread (berapa banyak proses paralel yang jalan sekaligus).

Siapkan list IP dan port 📝

Gabungkan IP dan port ke dalam kombinasi (ip, port) supaya bisa dicek satu-satu.

Bersihkan file hasil sebelumnya dan siapin folder 🗃️

Buat folder Result dan bersihin file Goodip.txt dan Badip.txt supaya hasil cek yang baru nggak campur sama yang lama.

Mulai pengecekan dengan multi-threading! ⚡

Program membuat pool thread sebanyak input user.
1. Setiap thread akan menjalankan fungsi check_ip_port yang bertugas menghubungi IP dan port.
2. Kalau port terbuka (connect berhasil), IP masuk ke file Goodip.txt.
3. Kalau port tertutup, masuk ke Badip.txt.
4. Kalau error, tampilkan pesan error.

Selesai! 🎉

Setelah semua selesai, program ngasih tahu kalau pengecekan sudah rampung dan hasilnya ada di folder Result.
