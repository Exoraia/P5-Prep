# Catatan MultiThread

## Apa itu MultiThreading?
<details>

Multithreading adalah pemrosesan beberapa program yang dijalankan secara paralel dalam waktu yang bersamaan. Multithreading juga merupakan salah satu contoh penerapan Asynchronous.

Asynchronous berarti program yang telah dijalankan tidak perlu selesai dieksekusi agar dapat melanjutkan ke tahap berikutnya. Dengan demikian, beberapa program atau kode dapat dieksekusi secara bersamaan.

Contoh sederhana dari multithreading adalah saat kita membuka beberapa tab di browser. Misalnya, kita dapat membuka YouTube di tab A dan Facebook di tab B secara bersamaan.

</details>

## Perbedaan Thread dan Runnable
<details>

### 1. Thread
- Merupakan superclass (induk) yang dapat di-extend oleh kelas lain agar dapat menjalankan perintah `start()`.
- Kekurangannya, dalam Java, sebuah class tidak dapat menjadi subclass dari dua superclass sekaligus (tidak mendukung multiple inheritance). Oleh karena itu, jika menggunakan `extends Thread`, kelas tersebut tidak dapat meng-extend kelas lain.

### 2. Runnable
- Merupakan sebuah interface yang dapat diimplementasikan oleh sebuah class agar dapat menjalankan perintah `run()`.
- Kelebihannya, Java memungkinkan sebuah class untuk mengimplementasikan lebih dari satu interface dan tetap dapat meng-extend kelas lain.

### Kesimpulan
Disarankan menggunakan `Runnable` karena lebih fleksibel. Namun, `Thread` juga dapat digunakan jika ingin langsung membuat thread dengan meng-extend kelas `Thread`.

</details>

## Penggunaan `Thread.sleep()`
<details>

`Thread.sleep()` merupakan metode dalam Java yang digunakan untuk memberikan jeda atau menunda eksekusi sebuah thread dalam satuan milidetik (1.000 milidetik = 1 detik). 

Fungsi ini berguna untuk mengontrol eksekusi multithreading agar kita dapat mengatur thread mana yang dijalankan terlebih dahulu sebelum thread lainnya ikut berjalan. Selain itu, `Thread.sleep()` dapat membantu dalam simulasi delay program maupun proses loading.

</details>