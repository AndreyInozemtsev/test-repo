##include <stdio.h>

int main() {
    int w = 80;
    int h = 25;
    int ball_start_x = w / 2;
    int ball_start_y = h / 2;
    int ball_y = ball_start_y;
    int ball_x = ball_start_x;
    int scring_x = 33;
    int scring_y = 3;
    int ri_1 = 1;
    int ri_2 = w - 2;
    int rstart_1 = 12;
    int rstart_2 = 12;
    int vector_x = -1;
    int vector_y = 1;
    int win = 21;
    int player1 = 0;
    int player2 = 0;
    char key;

    while (1) {
        printf("\33[0d\33[2J"); // очистка экрана

        for (int y = 0; y < h; y++) {
            for (int x = 0; x < w; x++) {
                if ((x == ri_1 && (y == rstart_1 - 1 || y == rstart_1 || y == rstart_1 + 1)) ||
                    (x == ri_2 && (y == rstart_2 - 1 || y == rstart_2 || y == rstart_2 + 1))) {
                    printf("|");
                } else if (x == ball_x && y == ball_y) {
                    printf("o");
                } else if ((y == 0 && x > 0 && x < w - 1) || (y == h - 1 && x > 0 && x < w - 1)) {
                    printf("-");
                } else if ((x == 0 && y > 0 && y < h - 1) ||
                           (x == w - 1 && y > 0 && y < h - 1 && y != 3) ||
                           ((x == w / 2) && (y != 3)) ||
                           (x == w - 3 && y == 3)) {
                    printf("|");
                } else if (x == w / 2 - 1 && y == 3) {
                    printf("|");
                } else if (y == scring_y && x == scring_x) {
                    printf("%02d", player1);
                    x++;
                } else if (y == scring_y && x == w - scring_x - 2) {
                    printf("%02d", player2);
                    x++;
                } else {
                    printf(" ");
                }
            }
            printf("\n");
        }

        // движение мяча
        if (ball_y == 1 || ball_y == h - 2) vector_y = -vector_y;
        if (ball_x == ri_1 + 1 && (ball_y == rstart_1 - 1 || ball_y == rstart_1 || ball_y == rstart_1 + 1))
            vector_x = -vector_x;
        if (ball_x == ri_2 - 1 && (ball_y == rstart_2 - 1 || ball_y == rstart_2 || ball_y == rstart_2 + 1))
            vector_x = -vector_x;

        ball_x += vector_x;  // по оси X
        ball_y += vector_y;  // по оси Y

        // табло
        if (ball_x < 2) {
            player2++;
            ball_x = ball_start_x;
            ball_y = ball_start_y;
        }
        if (ball_x > w - 2) {
            player1++;
            ball_x = ball_start_x;
            ball_y = ball_start_y;
        }
        if (player1 == win) {
            printf("Победил первый игрок\n");
            break;
        } else if (player2 == win) {
            printf("Победил второй игрок\n");
            break;
        }

        // движение ракеток
        key = getchar();
        if (key == 'a' && rstart_1 - 2 > 0) rstart_1--;
        if (key == 'z' && rstart_1 + 2 < h - 1) rstart_1++;
        if (key == 'k' && rstart_2 - 2 > 0) rstart_2--;
        if (key == 'm' && rstart_2 + 2 < h - 1) rstart_2++;
        if (key == 'q') return 0;
    }
}