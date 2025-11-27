# Ex.No:1
# Ex.Name:Write a CPP program to REVERSE the Singly Linked List using STL and Display the same.

## Aim:
To write a CPP program to REVERSE the Singly Linked List using STL and Display the same.


## Algorithm:
1. Start
2. Create a list container using STL
3. Read number of elements n
4. Insert elements into the list using push_back()
5. Display original list elements
6. Use reverse() function of STL to reverse the list
7. Display reversed list elements
8. Stop

## Program:
```
#include <iostream>
#include <forward_list>

using namespace std;

int main() 
{
    forward_list<int> sll = {10, 20, 40, 30, 70};

    cout << "List elements before performing reverse operation: ";
    
    for (const int& elem : sll)
    {
        cout << elem << " ";
    }
    cout << endl;

    sll.reverse();

    cout << "List elements after performing reverse operation: ";
    
    for (const int& elem : sll)
    {
        cout << elem << " ";
    }

    return 0;
}
```


## Output:
<img width="1220" height="314" alt="Screenshot 2025-10-11 132926" src="https://github.com/user-attachments/assets/06a31914-a54b-47e6-9676-8aff0c0756f0" />

## Result:
The Program Executed Successfully to REVERSE the Singly Linked List using STL and Display the same.


