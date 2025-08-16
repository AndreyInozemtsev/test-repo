#include <stdio.h>

int main() {
    int w = 80, h = 25;

    int ball_start_x = w / 2;
    int ball_start_y = h / 2;
    int ball_x = ball_start_x, ball_y = ball_start_y;

    int scring_x = 33, scring_y = 1;

    int first_player_pad_x = 1;
    int second_player_pad_x = w - 2;
    int first_player_pad_y_center = h / 2;
    int second_player_pad_y_center = h / 2;

    int vector_x = -1, vector_y = 1;
    int win = 21;
    int player1 = 0, player2 = 0;

    char key;
    while (1) {
        // очистка экрана
        printf("\033[H\033[J");

        // отрисовка
        for (int y = 0; y < h; y++) {
            for (int x = 0; x < w; x++) {
                if ((x == first_player_pad_x &&
                    (y == first_player_pad_y_center - 1 || y == first_player_pad_y_center || y == first_player_pad_y_center + 1)) ||
                    (x == second_player_pad_x &&
                    (y == second_player_pad_y_center - 1 || y == second_player_pad_y_center || y == second_player_pad_y_center + 1))) {
                    printf("|");  // ракетки
                } else if (x == ball_x && y == ball_y) {
                    printf("o");  // мяч
                } else if (y == 0 || y == h-1) {
                    printf("-");  // верх/низ
                } else if (x == 0 || x == w-1 || x == w/2) {
                    printf("|");  // границы + центр
                } else if (x == scring_x && y == scring_y) {
                    printf("%02d", player1); x++;
                } else if (x == (w - scring_x - 2) && y == scring_y) {
                    printf("%02d", player2); x++;
                } else {
                    printf(" ");
                }
            }
            printf("\n");
        }

        // движение мяча
        if (ball_y == 1 || ball_y == h-2) vector_y = -vector_y;
        if (ball_x == first_player_pad_x + 1 &&
            (ball_y == first_player_pad_y_center - 1 || ball_y == first_player_pad_y_center || ball_y == first_player_pad_y_center + 1))
            vector_x = -vector_x;
        if (ball_x == second_player_pad_x - 1 &&
            (ball_y == second_player_pad_y_center - 1 || ball_y == second_player_pad_y_center || ball_y == second_player_pad_y_center + 1))
            vector_x = -vector_x;

        ball_x += vector_x;
        ball_y += vector_y;

        // табло
        if (ball_x <= 0) {
            player2++;
            ball_x = ball_start_x; ball_y = ball_start_y;
        }
        if (ball_x >= w-1) {
            player1++;
            ball_x = ball_start_x; ball_y = ball_start_y;
        }
        if (player1 == win) { printf("Победил первый игрок\n"); break; }
        if (player2 == win) { printf("Победил второй игрок\n"); break; }

        // управление
        key = getchar();
        if (key == 'a' && first_player_pad_y_center > 2) first_player_pad_y_center--;
        if (key == 'z' && first_player_pad_y_center < h-3) first_player_pad_y_center++;
        if (key == 'k' && second_player_pad_y_center > 2) second_player_pad_y_center--;
        if (key == 'm' && second_player_pad_y_center < h-3) second_player_pad_y_center++;
        if (key == 'q') break;
    }
}