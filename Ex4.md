# Ex.No:4
# Ex.Name : Write a C++ function void addPolynomials(Node *head1,Node *head2) to add and display the sum of two polynomial expressions (  2x^4 5x^3 3x^2 and 4x^4 8x^3 7x^2  ) using Linked list concept.

## Aim:
To write a C++ function void addPolynomials(Node *head1,Node *head2) to add and display the sum of two polynomial expressions.

## Algorithm:
1. Start
2. Create linked lists for both polynomials
3. Compare powers of terms from both lists
4. If powers equal, add coefficients and store in result list
5. If one power is greater, copy that term to result list
6. Continue until both lists are processed
7. Display the resulting polynomial
8. Stop

## Program:
```
void addPolynomials(Node *head1,Node *head2)
{
    if(head1==NULL &&head2==NULL)
    {
        return;
    }
    else if(head1->power ==head2->power)
    {
        cout << " " << head1->coeff +  head2->coeff <<"x^" << head1->power << " ";
        addPolynomials(head1->next,head2->next);
    }
    else if(head1->power > head2->power)
    {
        cout << " " << head1->coeff <<"x^" << head1->power << " ";
        addPolynomials(head1->next, head2);
    }
    else
    {
        cout << " " << head2->coeff <<"x^" << head2->power << " ";
        addPolynomials(head1, head2->next);
    }
}
```


## Output:
<img width="640" height="379" alt="Screenshot 2025-10-11 134029" src="https://github.com/user-attachments/assets/9c181ae9-e341-4d07-a812-46191cd57a9c" />

## Result:
The Program Executed Successfully.
