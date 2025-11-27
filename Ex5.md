# Ex.No:5
# Ex.Name : Write a CPP program to SEARCH an element from the Circularly Linked List and Display the same.

## Aim:
To write a CPP program to SEARCH an element from the Circularly Linked List and Display the same.

## Algorithm:
1. Start
2. Create circular linked list nodes
3. Insert each element using insert() function
4. Traverse the list circularly using do-while loop
5. Compare each node’s data with search key
6. If match found, display “Element found”
7. If full circle completes with no match, display “Not found”
8. Stop

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

void Search(int d1)
{
    temp = head;
    bool ans = 0;
    for(int i = 0;i<5;i++)
    {
        
        if(temp->data == d1)
        {
            ans  = 1;
            break;
        }
        else
        {
            temp = temp->nextptr;
        }
    }
    if(ans == 1)
    {
        cout<<"Element "<<d1<<" Found";
    }
    else
    {
        cout<<"Element not Found";
    }
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
    Search(d1);
    
}
```

## Output:
<img width="1204" height="445" alt="Screenshot 2025-10-11 134424" src="https://github.com/user-attachments/assets/0d1471b4-2e45-4958-96f4-fd542838a68a" />

## Result:
The Program Executed Successfully.
