### 1.2 Understand How It Works

![Screenshot](/public/v1.2.png)

Fungsi async dijalankan di latar belakang tanpa menghentikan jalannya thread utama. Jadi, thread utama akan langsung lanjut ke baris kode berikutnya tanpa harus menunggu fungsi async selesai. Fungsi async tetap dieksekusi sesuai urutan pemanggilannya, tapi tidak memblokir eksekusi utama. Karena itu, output "hey hey" muncul lebih dulu dibanding "Howdy" dan "Done". Ketika spawner di-drop, itu menandakan bahwa program telah selesai dijalankan.

### 1.2  Multiple Spawn and removing drop

![Screenshot](/public/v1.3.png)

Tidak memakai `drop.spawner()` akan membuat program merasa bahwa prosesnya belum selesai. Akibatnya, program akan terus menunggu dan tidak akan berhenti atau keluar dengan sendirinya. Meskipun menggunakan banyak thread, eksekusinya tetap berjalan secara berurutan. Karena "hey hey" berada di luar blok async, maka ia akan dijalankan terlebih dahulu sebelum bagian async lainnya selesai.