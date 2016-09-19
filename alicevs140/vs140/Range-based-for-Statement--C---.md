---
title: "Range-based for Statement (C++)"
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
ms.assetid: 5750ba1d-ba48-4236-a923-e32de8345c2d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Range-based for Statement (C++)
Executes `statement` repeatedly and sequentially for each element in `expression`.  
  
## Syntax  
  
```  
  
      for ( for-range-declaration : expression )  
   statement   
```  
  
## Remarks  
 Use the range-based `for` statement to construct loops that must execute through a "range", which is defined as anything that you can iterate through—for example, `std::vector`, or any other STL sequence whose range is defined by a `begin()` and `end()`. The name that is declared in the `for-range-declaration` portion is local to the `for` statement and cannot be re-declared in `expression` or `statement`. Note that the [auto](../vs140/auto--C---.md) keyword is preferred in the `for-range-declaration` portion of the statement.  
  
 This code shows how to use ranged `for` loops to iterate through an array and a vector:  
  
```cpp  
  
// range-based-for.cpp  
// compile by using: cl /EHsc /nologo /W4  
#include <iostream>  
#include <vector>  
using namespace std;  
  
int main()   
{  
    // Basic 10-element integer array.  
    int x[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };  
  
    // Range-based for loop to iterate through the array.  
    for( int y : x ) { // Access by value using a copy declared as a specific type.   
                       // Not preferred.  
        cout << y << " ";  
    }  
    cout << endl;  
  
    // The auto keyword causes type inference to be used. Preferred.  
  
    for( auto y : x ) { // Copy of 'x', almost always undesirable  
        cout << y << " ";  
    }  
    cout << endl;  
  
    for( auto &y : x ) { // Type inference by reference.  
        // Observes and/or modifies in-place. Preferred when modify is needed.  
        cout << y << " ";  
    }  
    cout << endl;  
  
    for( const auto &y : x ) { // Type inference by reference.  
        // Observes in-place. Preferred when no modify is needed.  
        cout << y << " ";  
    }  
    cout << endl;  
    cout << "end of integer array test" << endl;  
    cout << endl;  
  
    // Create a vector object that contains 10 elements.  
    vector<double> v;  
    for (int i = 0; i < 10; ++i) {  
        v.push_back(i + 0.14159);  
    }  
  
    // Range-based for loop to iterate through the vector, observing in-place.  
    for( const auto &j : v ) {  
        cout << j << " ";  
    }  
    cout << endl;  
    cout << "end of vector test" << endl;  
}  
  
```  
  
 Here is the output:  
  
 `1 2 3 4 5 6 7 8 9 10`  
  
 `1 2 3 4 5 6 7 8 9 10`  
  
 `1 2 3 4 5 6 7 8 9 10`  
  
 `1 2 3 4 5 6 7 8 9 10`  
  
 `end of integer array test`  
  
 `0.14159 1.14159 2.14159 3.14159 4.14159 5.14159 6.14159 7.14159 8.14159 9.14159`  
  
 `end of vector test`  
  
 A range-based `for` loop terminates when one of these in `statement` is executed: a [break](../vs140/break-Statement--C---.md), [return](../vs140/return-Statement--C---.md), or [goto](../vs140/goto-Statement--C---.md) to a labeled statement outside the range-based **for** loop. A [continue](../vs140/continue-Statement--C---.md) statement in a range-based `for` loop terminates only the current iteration.  
  
 Keep in mind these facts about range-based `for`:  
  
-   Automatically recognizes arrays.  
  
-   Recognizes containers that have `.begin()` and `.end()`.  
  
-   Uses argument-dependent lookup `begin()` and `end()` for anything else.  
  
## See Also  
 [auto](../vs140/auto--C---.md)   
 [Iteration Statements](../vs140/Iteration-Statements--C---.md)   
 [Keywords](../vs140/Keywords--C---.md)   
 [while Statement (C++)](../vs140/while-Statement--C---.md)   
 [do-while Statement (C++)](../vs140/do-while-Statement--C---.md)   
 [for](../vs140/for-Statement--C---.md)