
//Autor: Daniel Antônio Faria
//BubbleSort em C.
#include <stdio.h>
#include <stdlib.h>

void bubble_sort(int a[], int n) {
    int i, j;
    for (i = 0; i < n - 1; i++) {
        for (j = 0; j < n - i - 1; j++) {
            if (a[j] > a[j + 1]) {
                int temp = a[j];
                a[j] = a[j + 1];
                a[j + 1] = temp;
            }
        }
    }
}

void mostrar_vetor(int a[], int n){
    int i;
    for(i = 0; i < n; i++){
        printf("%d, ", a[i]);
    }
    printf("\n");
}

//código de testes
int main() {
    int c[10] = {9 , 10 , -1, 3, 6, 2, 1, -3, 1, 0, -2, 15, 8, -7, 0};
    bubble_sort(c, 15);
    mostrar_vetor(c, 15);
    return 0;
}
