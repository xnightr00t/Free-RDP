# Windows RDP via Ngrok

Aksi ini memungkinkan Anda untuk membuat koneksi **Remote Desktop Protocol (RDP)** ke runner Windows GitHub selama maksimal **6 jam** menggunakan **Ngrok** (TCP tunneling).

---

## 🧰 Prasyarat

1. **Akun [Ngrok](https://ngrok.com/)**
2. **Ngrok Auth Token**

---

## 🔐 Mendapatkan Ngrok Auth Token

1. Daftar atau login di: [https://dashboard.ngrok.com/](https://dashboard.ngrok.com/)
2. Buka menu **Auth > Your Authtoken**
3. Salin token, contoh: *1qg5eJzK4A9Xx1aBcDefGhIJKLmNoPQRsTuVWxyZ*
4. Di repository GitHub kamu, buka:
- **Settings > Secrets and variables > Actions > New repository secret**
- Tambahkan secret dengan:
  - **Name:** `NGROK_AUTH_TOKEN`
  - **Value:** `token_anda`

---

## 📦 Cara Instalasi

1. Fork repository ini dari GitHub
2. Buka repo hasil fork:  
`https://github.com/<username-kamu>/<repo-kamu>`
3. Buka tab **Actions** → pilih workflow `Windows RDP via Ngrok`
4. Klik tombol **Run workflow**

---

## 💻 Login ke RDP

1. Buka Remote Desktop (di Windows tekan `Win+R` → ketik `mstsc`)
2. Masukkan:
- **Computer:** `xyz.ngrok.io:12345`
- **Username:** `Adminxnight`
- **Password:** `Adminnight123`
3. Klik Connect dan klik **Yes** jika ada peringatan sertifikat

---

## 🕒 Catatan

- Sesi RDP hanya aktif selama **maksimal 6 jam**
- VM bersifat sementara (tidak ada penyimpanan permanen)
- User akan hilang saat workflow selesai

---

**❌ Jangan gunakan untuk aktivitas yang melanggar [Terms of Service GitHub](https://docs.github.com/en/actions/concepts/runners/github-hosted-runners#usage-limits)**

---
