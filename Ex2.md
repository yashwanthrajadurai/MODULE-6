# Ex.No:2
# Ex.Name : Write a CPP Program to INSERT 5 data's into Doubly Linked List Using STL and Display the same.

## Aim:
To write a CPP Program to INSERT 5 data's into Doubly Linked List Using STL and Display the same.

## Algorithm:
1. Start
2. Create a doubly linked list using list<int>
3. Read 5 data elements from user
4. Insert each element using push_back()
5. Traverse the list using a for-each loop
6. Display all elements
7. Stop
   
## Program:
```
#include <iostream>
#include <list>

using namespace std;

int main() 
{
    list<int> gqlist1;
    int input;

    
    for (int i = 0; i < 5; ++i) 
    {
        cin >> input;
        gqlist1.push_back(input);
    }

    cout << "List 1 (gqlist1) is :  ";
    
    for (int value : gqlist1) 
    {
        cout << value << " ";
    }
    cout << endl;

    return 0;
}
```


## Output:
<img width="1176" height="332" alt="Screenshot 2025-10-11 133403" src="https://github.com/user-attachments/assets/62316a4a-ad77-4ddc-9796-1ba0aba574d7" />

## Result:
The Program Executed Successfully to INSERT 5 data's into Doubly Linked List Using STL and Display the same.
