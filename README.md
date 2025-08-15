#include <stdio.h>
#include <math.h>

int main(void) {
    const int N = 42;
    const double pi = 3.14159265358979323846;
    const double step = (2.0 * pi) / (N - 1);

    for (int i = 0; i < N; i++) {
        double x = -pi + i * step;
        double y_verseier = -1.0;
        double y_lemniscate = -1.0;
        double y_hyperbola = -1.0;

        // Верзьера Аньези
        y_verseier = 1.0 / (1.0 + x * x);

        // Лемниската Бернулли
        double inner = sqrt(1.0 + 4.0 * x * x) - x * x - 1.0;
        if (inner >= 0.0)
            y_lemniscate = sqrt(inner);

        // Квадратичная гипербола
        if (x != 0.0)
            y_hyperbola = 1.0 / (x * x);

        // Вывод
        printf("%.7f | ", x);

        if (y_verseier >= 0.0)
            printf("%.7f | ", y_verseier);
        else
            printf("- | ");

        if (y_lemniscate >= 0.0)
            printf("%.7f | ", y_lemniscate);
        else
            printf("- | ");

        if (y_hyperbola >= 0.0)
            printf("%.7f", y_hyperbola);
        else
            printf("-");

        printf("\n");
    }

    return 0;
} 