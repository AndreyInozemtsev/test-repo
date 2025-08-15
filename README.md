#include <stdio.h>

int is_prime(int n) {
    if (n < 2)
        return 0;
    for (int i = 2; i < n; i++) {
        int temp = n;
        while (temp >= i) // эмуляция temp % i
            temp -= i;
        if (temp == 0)
            return 0; // делится, значит не простое
    }
    return 1;
}

int find_largest_prime_divisor(int a) {
    if (a < 0) // берём модуль
        a = -a;
    if (a == 0 || a == 1)
        return -1;

    int largest = 1;
    for (int i = 2; i <= a; i++) {
        int temp = a;
        while (temp >= i) // проверка делимости
            temp -= i;
        if (temp == 0 && is_prime(i))
            largest = i;
    }
    return largest;
}

int main(void) {
    int a;
    if (scanf("%d", &a) != 1) {
        printf("n/a");
        return 0;
    }
    int res = find_largest_prime_divisor(a);
    if (res == -1)
        printf("n/a");
    else
        printf("%d", res);
    return 0;
}