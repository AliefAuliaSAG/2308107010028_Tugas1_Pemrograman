SOAL 2
#include <stdio.h>

Ini adalah preprocessor directive yang menye `<stdio.h>`, yang diperlukan untuk menggunakan fungsi input-output standar dalam bahasa C seperti `printf()` dan `scanf()`.


int main() {
    int tahun;

Di sini, fungsi `main()` didefinisikan. Ini adalah titik masuk utama dari program C. Variabel `tahun` dideklarasikan sebagai variabel untuk menyimpan tahun yang dimasukkan oleh pengguna.


    // Meminta input tahun dari pengguna
    while (1) {
        printf("Masukkan tahun: ");


Program memulai loop tak terbatas (`while (1)`) untuk terus meminta input tahun dari pengguna. Pesan `"Masukkan tahun (format: YYYY): "` dicetak ke layar untuk memberi petunjuk kepada pengguna.


        if (scanf("%d", &tahun) != 1) {
            while (getchar() != '\n'); // Membersihkan input buffer
            printf("Input harus berupa bilangan. Silakan coba lagi.\n");


Pertama, program mencoba membaca input menggunakan `scanf()`. Jika `scanf()` gagal membaca angka bulat (`%d`), kondisi `if` akan dieksekusi. Dalam kondisi tersebut, program membersihkan sisa input dari buffer menggunakan `getchar()` dan menampilkan pesan kesalahan kepada pengguna.


        } else if (tahun < 1000 || tahun > 9999) {
            printf("Tahun harus terdiri dari 4 angka. Silakan coba lagi.\n");

Jika input tahun yang dimasukkan oleh pengguna tidak sesuai dengan format yang diinginkan (yaitu 4 digit), program akan menampilkan pesan kesalahan.


        } else {
            break;
        }

Jika input tahun sesuai dengan format yang diinginkan, program akan keluar dari loop dengan menggunakan pernyataan `break`.


    // Memeriksa apakah tahun kabisat atau bukan
    if ((tahun % 4 == 0 && tahun % 100 != 0) || (tahun % 400 == 0)) {
        printf("%d adalah tahun kabisat.\n", tahun);
    } else {
        printf("%d bukan tahun kabisat.\n", tahun);
    }

Setelah mendapatkan input tahun yang valid dari pengguna, program melakukan pengecekan apakah tahun tersebut merupakan tahun kabisat atau bukan. Pengecekan dilakukan dengan aturan-aturan yang berlaku untuk tahun kabisat. Hasil pengecekan kemudian dicetak dan ditampilkan kepada pengguna.


    return 0;
}

Akhirnya, fungsi `main()` mengembalikan nilai 0, menandakan bahwa program telah berakhir dengan sukses. Ini adalah standar dalam bahasa C untuk menunjukkan bahwa program telah selesai dengan baik.