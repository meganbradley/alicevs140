---
title: "break Statement (C++)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: 63739928-8985-4b05-93ce-016322e6da3d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# break Statement (C++)
The `break` statement ends execution of the nearest enclosing loop or conditional statement in which it appears. Control passes to the statement that follows the end of the statement, if any.  
  
## Syntax  
  
```  
break;  
```  
  
## Remarks  
 The `break` statement is used with the conditional [switch](../vs140/switch-Statement--C---.md) statement and with the [do](../vs140/do-while-Statement--C---.md), [for](../vs140/for-Statement--C---.md), and [while](../vs140/while-Statement--C---.md) loop statements.  
  
 In a `switch` statement, the `break` statement causes the program to execute the next statement outside the `switch` statement. Without a `break` statement, every statement from the matched `case` label to the end of the `switch` statement, including the `default` clause, is executed.  
  
 In loops, the `break` statement ends execution of the nearest enclosing `do`, `for`, or `while` statement. Control passes to the statement that follows the ended statement, if any.  
  
 Within nested statements, the `break` statement ends only the `do`, `for`, `switch`, or `while` statement that immediately encloses it. You can use a `return` or `goto` statement to transfer control from more deeply nested structures.  
  
## Example  
 The following code shows how to use the `break` statement in a `for` loop.  
  
```cpp  
#include <iostream>  
using namespace std;  
  
int main()  
{  
    // An example of a standard for loop  
    for (int i = 1; i < 10; i++)  
    {  
        cout << i << '\n';  
        if (i == 4)  
            break;  
    }  
  
    // An example of a range-based for loop  
int nums []{1, 2, 3, 4, 5, 6, 7, 8, 9, 10};  
  
    for (int i : nums) {  
        if (i == 4) {  
            break;  
        }  
        cout << i << '\n';  
    }  
}  
```  
  
 **In each case:**   
**1**  
**2**  
**3** The following code shows how to use `break` in a `while` loop and a `do` loop.  
  
```cpp  
  
#include <iostream>  
using namespace std;  
  
int main() {  
    int i = 0;  
  
    while (i < 10) {  
        if (i == 4) {  
            break;  
        }  
        cout << i << '\n';  
        i++;  
    }  
  
    i = 0;  
    do {  
        if (i == 4) {  
            break;  
        }  
        cout << i << '\n';  
        i++;  
    } while (i < 10);  
}  
```  
  
 **In each case:**  
**0123** The following code shows how to use `break` in a switch statement. You must use `break` in every case if you want to handle each case separately; if you do not use `break`, the code execution falls through to the next case.  
  
```cpp  
#include <iostream>  
using namespace std;  
  
enum Suit{ Diamonds, Hearts, Clubs, Spades };  
  
int main() {  
  
    Suit hand;  
    . . .  
    // Assume that some enum value is set for hand  
    // In this example, each case is handled separately  
    switch (hand)  
    {  
    case Diamonds:  
        cout << "got Diamonds \n";  
        break;  
    case Hearts:  
        cout << "got Hearts \n";  
        break;  
    case Clubs:  
        cout << "got Clubs \n";  
        break;  
    case Spades:  
        cout << "got Spades \n";  
        break;  
    default:   
          cout << "didn't get card \n";  
    }  
    // In this example, Diamonds and Hearts are handled one way, and  
    // Clubs, Spades, and the default value are handled another way  
    switch (hand)  
    {  
    case Diamonds:  
    case Hearts:  
        cout << "got a red card \n";  
        break;  
    case Clubs:  
    case Spades:   
    default:  
        cout << "didn't get a red card \n";  
    }  
}  
```  
  
## See Also  
 [Jump Statements](../vs140/Jump-Statements--C---.md)   
 [Keywords](../vs140/Keywords--C---.md)   
 [continue Statement](../vs140/continue-Statement--C---.md)