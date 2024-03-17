Baik,saya akan menjelaskan setiap bagian kode dari case 1 hingga case 4:

### Case 1: Konversi dari Desimal ke Biner
```c
case 1:
    printf("Masukkan bilangan desimal: ");
    scanf("%ld", &bilangan);

    // Konversi dari Desimal ke Biner
    {
        long int binaryNumber = 0, base = 1;
        int remainder;

        while (bilangan > 0) {
            remainder = bilangan % 2;
            binaryNumber = binaryNumber + remainder * base;
            bilangan = bilangan / 2;
            base = base * 10;
        }

        printf("Biner: %ld\n", binaryNumber);
    }
    break;
```
1. Program meminta pengguna untuk memasukkan bilangan desimal.
2. Variabel `binaryNumber` digunakan untuk menyimpan nilai biner hasil konversi dari bilangan desimal.
3. Variabel `base` digunakan untuk menentukan posisi digit biner (basis 2).
4. Selama `bilangan` (bilangan desimal) masih lebih dari 0, dilakukan iterasi dalam sebuah loop while.
5. Pada setiap iterasi, sisa pembagian `bilangan` dengan 2 (hasil modulo `% 2`) disimpan dalam variabel `remainder`.
6. `remainder` kemudian dikalikan dengan `base` dan ditambahkan ke `binaryNumber`.
7. Nilai `bilangan` kemudian dibagi dengan 2 untuk melanjutkan proses konversi.
8. `base` kemudian diperbarui dengan mengalikannya dengan 10, karena kita melakukan konversi dari biner (basis 2) ke desimal (basis 10).
9. Setelah proses iterasi selesai, nilai biner hasil konversi ditampilkan ke layar.

### Case 2: Konversi dari Biner ke Desimal
```c
case 2:
    printf("Masukkan bilangan biner: ");
    scanf("%ld", &bilangan);

    // Konversi dari Biner ke Desimal
    {
        long int decimal = 0, base = 1, temp;

        while (bilangan > 0) {
            temp = bilangan % 10;
            decimal += temp * base;
            base = base * 2;
            bilangan = bilangan / 10;
        }

        printf("Desimal: %ld\n", decimal);
    }
    break;
```
1. Program meminta pengguna untuk memasukkan bilangan biner.
2. Variabel `decimalNumber` digunakan untuk menyimpan nilai desimal hasil konversi dari bilangan biner.
3. Variabel `base` digunakan untuk menentukan posisi digit desimal (basis 10).
4. Selama `bilangan` (bilangan biner) masih lebih dari 0, dilakukan iterasi dalam sebuah loop while.
5. Pada setiap iterasi, digit terakhir dari bilangan biner (yang diperoleh dengan menggunakan modulo `% 10`) disimpan dalam variabel `temp`.
6. Digit tersebut kemudian ditambahkan ke `decimal` setelah dikalikan dengan `base`.
7. Nilai `base` kemudian diperbarui dengan mengalikannya dengan 2, karena kita melakukan konversi dari biner (basis 2) ke desimal (basis 10).
8. `bilangan` kemudian dibagi dengan 10 untuk menghapus digit terakhir yang telah diproses dalam konversi.
9. Setelah proses iterasi selesai, nilai desimal hasil konversi ditampilkan ke layar.

### Case 3: Konversi dari Desimal ke Octal
```c
case 3:
    printf("Masukkan bilangan desimal: ");
    scanf("%ld", &bilangan);

    // Konversi dari Desimal ke Octal
    {
        long int octalNumber = 0, base = 1;
        int remainder;

        while (bilangan > 0) {
            remainder = bilangan % 8;
            octalNumber = octalNumber + remainder * base;
            bilangan = bilangan / 8;
            base = base * 10;
        }

        printf("Octal: %ld\n", octalNumber);
    }
    break;
```
1. Program meminta pengguna untuk memasukkan bilangan desimal.
2. Variabel `octalNumber` digunakan untuk menyimpan nilai oktal hasil konversi dari bilangan desimal.
3. Variabel `base` digunakan untuk menentukan posisi digit oktal (basis 8).
4. Selama `bilangan` (bilangan desimal) masih lebih dari 0, dilakukan iterasi dalam sebuah loop while.
5. Pada setiap iterasi, sisa pembagian `bilangan` dengan 8 (hasil modulo `% 8`) disimpan dalam variabel `remainder`.
6. `remainder` kemudian dikalikan dengan `base` dan ditambahkan ke `octalNumber`.
7. Nilai `bilangan` kemudian dibagi dengan 8 untuk melanjutkan proses konversi.
8. `base` kemudian diperbarui dengan mengalikannya dengan 10, karena kita melakukan konversi dari oktal (basis 8) ke desimal (basis 10).
9. Setelah proses iterasi selesai, nilai oktal hasil konversi ditampilkan ke layar.

### Case 4: Konversi dari Octal ke Desimal
```c
case 4:
    printf("Masukkan bilangan octal: ");
    scanf("%ld", &bilangan);

    // Konversi dari Octal ke Desimal
    {
        long int decimal = 0, base = 1, temp;

        while (bilangan > 0) {
            temp = bilangan % 10;
            decimal += temp * base;
            base = base * 8;
            bilangan = bilangan / 10;
        }

        printf("Desimal: %ld\n", decimal);
    }
    break;
```
1. Program meminta pengguna untuk memasukkan bilangan oktal.
2. Variabel `decimal` digunakan untuk menyimpan nilai desimal hasil konversi dari bilangan oktal.
3. Variabel `base` digunakan untuk menentukan posisi digit desimal (basis 10).
4. Selama `bilangan` (bilangan oktal) masih lebih dari 0, dilakukan iterasi dalam sebuah loop while.
5. Pada setiap iterasi, digit terakhir dari bilangan oktal (yang diperoleh dengan menggunakan modulo `% 10`) disimpan dalam variabel `temp`.
6. Digit tersebut kemudian ditambahkan ke `decimal` setelah dikalikan dengan `base`.
7. Nilai `base` kemudian diperbarui dengan mengalikannya dengan 8, karena kita melakukan konversi dari oktal