#include <stdio.h>
#define MAX 6

int box[MAX];
int top = -1;

void push(int x) {
    if (top == MAX - 1) {
        printf("Stack is Full!!\n");
    } else {
        top++;
        box[top] = x;
        printf("Value %d has been added\n", x);
    }
}

void pop() {
    if (top == -1) {
        printf("Stack is Empty!!\n");
    } else {
        int x = box[top--];
        printf("%d has been removed\n", x);
    }
}

int main() {
    push(10);
    push(20);
    push(30);
    push(40);
    push(50);
    push(60);
    push(70);   // Full

    pop();
    pop();
    pop();
    pop();
    pop();
    pop();
    pop();      // Empty

    return 0;
}
