#include <stdio.h>

float tambah(float x, float y) {
    return x + y;
}

float kurang(float x, float y) {
    return x - y;
}

float kali(float x, float y) {
    return x * y;
}

float bagi(float x, float y) {
    return x / y;
}

int main() {
    int pilihan;
    float angka1,angka2;

    printf("pilih operasi:\n");
    printf("1. Tambah\n");
    printf("2. Kurang\n");
    printf("3. kali\n");
    printf("4. bagi\n");

    printf("Masukkan pilihan (1/2/3/4):");
    scanf("%d",&pilihan);
    printf("Masukkan Angka Pertama:");
    scanf("%d",&angka1);

    printf("Masukkan angka kedua:");
    scanf("%d",&angka2);
    
    switch (pilihan) {
        case 1:
            printf("Hasil: %.2f\n", tambah(angka1,angka2));
             break;
        case 2:
             printf("Hasil: %.2f\n", kurang(angka1,angka2));
             break;
         case 3:
             printf("Hasil: %.2f\n", kali(angka1,angka2));
             break;
          case 4:
             if (angka2 != 0) {
                 printf("Hasil: %.2f\n",bagi(angka1,angka2));
             } else {
                 printf("ERROR: Pembagian Dengan Nol tidak diperbolehkan!\n");
             }
             break;
             default: 
             printf("Pilihan tidak valid!\n");
        
    }
    
    return 0;
}
