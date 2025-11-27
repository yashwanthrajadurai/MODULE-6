# Ex.No:3
# Ex.Name : Write a CPP Program to INSERT an element in the FRONT to a Circularly Linked List and Display the same.

## Aim:
To write a CPP Program to INSERT an element in the FRONT to a Circularly Linked List and Display the same.

## Algorithm:
1. Start
2. Create a list container to represent a circular linked list
3. Read total number of elements n
4.Insert n elements using push_back()
5. Read element to insert at front
6. Use push_front() to add it to the beginning
7. Display all list elements
8. Print the first element again to simulate circular link
9. Stop

## Program:
```
#include<iostream>
using namespace std;

class Node
{
    public:
    int data;
    Node *nextptr;
}*head,*tail,*newn,*temp;

void display()
{
    temp = head;
    do
    {
        cout<<"Data = "<<temp->data<<" ";
        temp = temp->nextptr;
    }
    while(temp->nextptr!=head);
    cout<<"Data = "<<temp->data<<" ";
    cout<<endl;
}

void createNode(int n)
{
    newn = new Node();
    newn->data = n;
    newn->nextptr = 0;
    
    if(head==0)
    {
        head = newn;
        tail = newn;
    }
    
    else
    {
        tail->nextptr = newn;
        tail = newn;
        tail->nextptr = head;
    }
}

void insert(int d1)
{
    temp = head;
    newn = new Node();
    newn->data = d1;
    newn->nextptr = temp;
    head = newn;
    tail->nextptr = head;
}

int main()
{
    int n;
    for(int i=0;i<5;i++)
    {
        cin>>n;
        createNode(n);
    }
    
    int d1;
    cin>>d1;
    display();
    insert(d1);
    display();
}
```


## Output:
<img width="1191" height="384" alt="Screenshot 2025-10-11 133723" src="https://github.com/user-attachments/assets/9906b44f-1119-48fb-b5c6-eda2b60b3798" />

## Result:
The Program Executed Successfully to INSERT an element in the FRONT to a Circularly Linked List and Display the same.
