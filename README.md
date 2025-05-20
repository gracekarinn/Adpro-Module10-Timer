### 1.2 Understand How It Works

![Screenshot](/public/v1.2.png)

Fungsi async dijalankan di latar belakang tanpa menghentikan jalannya thread utama. Jadi, thread utama akan langsung lanjut ke baris kode berikutnya tanpa harus menunggu fungsi async selesai. Fungsi async tetap dieksekusi sesuai urutan pemanggilannya, tapi tidak memblokir eksekusi utama. Karena itu, output "hey hey" muncul lebih dulu dibanding "Howdy" dan "Done". Ketika spawner di-drop, itu menandakan bahwa program telah selesai dijalankan.

