#include <iostream>
using namespace std;

class Queue {
    int queue[5];
    int front, rear;

public:

    void initialize() {
        front = -1;
        rear = -1;
    }

    void Enqueue(int info) {
        if (rear == 4) {
            cout << "Queue is full";
            return;
        }

        if (front == -1)
            front = 0;

        rear++;
        queue[rear] = info;
    }

    void Dequeue() {
        if (IsEmpty()) {
            cout << "Queue is empty";
            return;
        }

        cout << "Deleted: " << queue[front];
        front++;

        if (front > rear) {
            front = -1;
            rear = -1;
        }
    }

    void Display() {
        if (IsEmpty()) {
            cout << "Queue is empty";
            return;
        }

        cout << "Queue: ";

        for (int i = front; i <= rear; i++) {
            cout << queue[i] << " ";
        }
    }

    bool IsEmpty() {
        return front == -1;
    }

    bool IsFull() {
        return rear == 4;
    }
};

int main() {

    Queue Q;

    Q.initialize();

    int ch, info;

    do {

        cout << "\n1> Enqueue";
        cout << "\n2> Dequeue";
        cout << "\n3> Display";
        cout << "\n4> IsEmpty";
        cout << "\n5> IsFull";
        cout << "\n6> Exit";

        cout << "\nEnter your choice: ";
        cin >> ch;

        switch (ch) {

            case 1:
                cout << "Enter value: ";
                cin >> info;
                Q.Enqueue(info);
                break;

            case 2:
                Q.Dequeue();
                break;

            case 3:
                Q.Display();
                break;

            case 4:
                if (Q.IsEmpty())
                    cout << "Queue is empty";
                else
                    cout << "Queue is not empty";
                break;

            case 5:
                if (Q.IsFull())
                    cout << "Queue is full";
                else
                    cout << "Queue is not full";
                break;

            case 6:
                cout << "Exiting...";
                break;

            default:
                cout << "Invalid choice";
        }

    } while (ch != 6);

    return 0;
}