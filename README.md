max.c:3:17: warning: code should be clang-formatted [-Wclang-format-violations]
int main(void) {
                ^
max.c:4:13: warning: code should be clang-formatted [-Wclang-format-violations]
  int a = 0;
            ^
max.c:5:13: warning: code should be clang-formatted [-Wclang-format-violations]
  int b = 0;
            ^
max.c:6:37: warning: code should be clang-formatted [-Wclang-format-violations]
  if (scanf("%d %d", &a, &b) != 2) {
                                    ^
max.c:7:21: warning: code should be clang-formatted [-Wclang-format-violations]
    printf("n/a\n");
                    ^
max.c:8:11: warning: code should be clang-formatted [-Wclang-format-violations]
  } else {
          ^
max.c:9:9: warning: code should be clang-formatted [-Wclang-format-violations]
    if ( a > b ) {
        ^
max.c:9:15: warning: code should be clang-formatted [-Wclang-format-violations]
    if ( a > b ) {
              ^
max.c:9:19: warning: code should be clang-formatted [-Wclang-format-violations]
    if ( a > b ) {
                  ^
max.c:10:25: warning: code should be clang-formatted [-Wclang-format-violations]
      printf("%d\n", a);
                        ^
max.c:11:13: warning: code should be clang-formatted [-Wclang-format-violations]
    } else {
            ^
max.c:12:25: warning: code should be clang-formatted [-Wclang-format-violations]
      printf("%d\n", b);
                        ^
max.c:13:6: warning: code should be clang-formatted [-Wclang-format-violations]
    }


arithmetic.c:8:13: warning: code should be clang-formatted [-Wclang-format-violations]
int main() {
            ^
arithmetic.c:9:12: warning: code should be clang-formatted [-Wclang-format-violations]
  int a, b;
           ^
arithmetic.c:10:5: warning: code should be clang-formatted [-Wclang-format-violations]
  if(scanf("%d %d", &a, &b) != 2) {
    ^
arithmetic.c:10:36: warning: code should be clang-formatted [-Wclang-format-violations]
  if(scanf("%d %d", &a, &b) != 2) {
                                   ^
arithmetic.c:11:48: warning: code should be clang-formatted [-Wclang-format-violations]
    printf("Error: you need to enter numbers");
                                               ^
arithmetic.c:12:4: warning: code should be clang-formatted [-Wclang-format-violations]
  }
   ^
arithmetic.c:14:67: warning: code should be clang-formatted [-Wclang-format-violations]
  printf("%d %d %d ", sum(a, b), substract(a, b), multiply(a, b));
                                                                  ^
arithmetic.c:15:7: warning: code should be clang-formatted [-Wclang-format-violations]
  if ( b != 0 ) {
      ^
arithmetic.c:15:14: warning: code should be clang-formatted [-Wclang-format-violations]
  if ( b != 0 ) {
             ^
arithmetic.c:15:18: warning: code should be clang-formatted [-Wclang-format-violations]
  if ( b != 0 ) {
                 ^
arithmetic.c:16:34: warning: code should be clang-formatted [-Wclang-format-violations]
    printf("%d\n", divide(a, b));
                                 ^
arithmetic.c:17:11: warning: code should be clang-formatted [-Wclang-format-violations]
  } else {
          ^
arithmetic.c:18:21: warning: code should be clang-formatted [-Wclang-format-violations]
    printf("n/a\n");
                    ^
arithmetic.c:19:4: warning: code should be clang-formatted [-Wclang-format-violations]
  }
   ^
arithmetic.c:23:30: warning: code should be clang-formatted [-Wclang-format-violations]
int substract(int a, int b) {
                             ^
arithmetic.c:24:18: warning: code should be clang-formatted [-Wclang-format-violations]
  return (a - b);
                 ^
arithmetic.c:27:29: warning: code should be clang-formatted [-Wclang-format-violations]
int multiply(int a, int b) {
                            ^
arithmetic.c:28:11: warning: code should be clang-formatted [-Wclang-format-violations]
  return ( a * b );
          ^
arithmetic.c:28:17: warning: code should be clang-formatted [-Wclang-format-violations]
  return ( a * b );
                ^
arithmetic.c:28:20: warning: code should be clang-formatted [-Wclang-format-violations]
  return ( a * b );
                   ^
arithmetic.c:31:27: warning: code should be clang-formatted [-Wclang-format-violations]
int divide(int a, int b) {
                          ^
arithmetic.c:32:11: warning: code should be clang-formatted [-Wclang-format-violations]
  return ( a / b );
          ^
arithmetic.c:32:17: warning: code should be clang-formatted [-Wclang-format-violations]
  return ( a / b );
                ^
arithmetic.c:32:20: warning: code should be clang-formatted [-Wclang-format-violations]
  return ( a / b );
                   ^
arithmetic.c:35:24: warning: code should be clang-formatted [-Wclang-format-violations]
int sum(int a, int b) {
                       ^
arithmetic.c:36:18: warning: code should be clang-formatted [-Wclang-format-violations]
  return (a + b);
                 ^
crack.c:3:17: warning: code should be clang-formatted [-Wclang-format-violations]
int main(void) {
                ^
crack.c:4:11: warning: code should be clang-formatted [-Wclang-format-violations]
  float a;
          ^
crack.c:5:11: warning: code should be clang-formatted [-Wclang-format-violations]
  float b; 
          ^
crack.c:6:74: warning: code should be clang-formatted [-Wclang-format-violations]
  printf("Enter a numbers with floating points separated by a space:\n");
                                                                         ^
crack.c:7:7: warning: code should be clang-formatted [-Wclang-format-violations]
  if ( scanf("%f %f", &a, &b) != 2 ) {
      ^
crack.c:7:35: warning: code should be clang-formatted [-Wclang-format-violations]
  if ( scanf("%f %f", &a, &b) != 2 ) {
                                  ^
crack.c:7:39: warning: code should be clang-formatted [-Wclang-format-violations]
  if ( scanf("%f %f", &a, &b) != 2 ) {
                                      ^
crack.c:8:21: warning: code should be clang-formatted [-Wclang-format-violations]
    printf("n/a\n");
                    ^
crack.c:9:11: warning: code should be clang-formatted [-Wclang-format-violations]
  } else {
          ^
crack.c:10:9: warning: code should be clang-formatted [-Wclang-format-violations]
    if ( a * a + b * b <= 25 ) {
        ^
crack.c:10:29: warning: code should be clang-formatted [-Wclang-format-violations]
    if ( a * a + b * b <= 25 ) {
                            ^
crack.c:10:33: warning: code should be clang-formatted [-Wclang-format-violations]
    if ( a * a + b * b <= 25 ) {
                                ^
crack.c:11:26: warning: code should be clang-formatted [-Wclang-format-violations]
      printf("GOTCHA\n");
                         ^
crack.c:12:13: warning: code should be clang-formatted [-Wclang-format-violations]
    } else {
            ^
crack.c:13:24: warning: code should be clang-formatted [-Wclang-format-violations]
      printf("MISS\n");
                       ^
crack.c:14:6: warning: code should be clang-formatted [-Wclang-format-violations]
    }
     ^
crack.c:15:4: warning: code should be clang-formatted [-Wclang-format-violations]
  }
   ^
hello.c:3:15: warning: code should be clang-formatted [-Wclang-format-violations]
int main(void){
              ^
hello.c:3:16: warning: code should be clang-formatted [-Wclang-format-violations]
int main(void){
               ^
hello.c:4:26: warning: code should be clang-formatted [-Wclang-format-violations]
  printf("Hello, AI!\n");
                         ^
