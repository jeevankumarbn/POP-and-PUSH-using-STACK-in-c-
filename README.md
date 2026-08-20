#include <iostream>

using namespace std;

void push(int stack[], int &top, int item)
{
    int max = 6;
    if (top >= max-1)
    {
        cout <<item << "Stack is Overflowing" << endl;
        return;
    }
    top = top+1;
    stack[top] = item;
    cout << item << "The items is pushed to Satck"<< endl;
}
    void pop(int stack[], int &top)
{
    if(top == -1)
    {
        cout<< " Stack is empty / underflow" << endl;
        return;
    }
    cout << stack[top] <<" is popped from the stack" <<endl;
    top = top-1;
 }


int main()
{
    int A[6];
    int top = -1;
    
    push(A, top, 56);
    push(A, top, 24);
    push(A, top, 32);
    push(A, top, 46);
    push(A, top, 37);
    push(A, top, 40);
    
    pop(A, top);
    pop(A, top);
    pop(A, top);
}
