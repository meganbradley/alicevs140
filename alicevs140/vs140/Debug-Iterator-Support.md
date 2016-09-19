---
title: "Debug Iterator Support"
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
ms.topic: article
ms.assetid: f3f5bd15-4be8-4d64-a4d0-8bc0761c68b6
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Debug Iterator Support
The Visual C++ run-time library detects incorrect iterator use, and asserts and displays a dialog box at run time. To enable debug iterator support, you must use a debug version of a C run-time library to compile your program. For more information, see [C Run-Time Libraries](../vs140/CRT-Library-Features.md). For information about how to use iterators, see [Checked Iterators](../vs140/Checked-Iterators.md).  
  
 The C++ standard describes how member functions might cause iterators to a container to become invalid. Two examples are:  
  
-   Erasing an element from a container causes iterators to the element to become invalid.  
  
-   Increasing the size of a [vector](../vs140/-vector-.md) (push or insert) causes iterators into the `vector` to become invalid.  
  
## Example  
 If you compile the following program in debug mode, at run time it will assert and terminate.  
  
```cpp  
/* compile with /EHsc /MDd */  
#include <vector>  
#include <iostream>  
  
int main() {  
   std::vector<int> v ;  
  
   v.push_back(10);  
   v.push_back(15);  
   v.push_back(20);  
  
   std::vector<int>::iterator i = v.begin();  
   ++i;  
  
   std::vector<int>::iterator j = v.end();  
   --j;  
  
   std::cout<<*j<<'\n';  
  
   v.insert(i,25);   
  
   std::cout<<*j<<'\n'; // Using an old iterator after an insert  
}  
```  
  
## Example  
 You can use the symbol [_HAS_ITERATOR_DEBUGGING](../vs140/_HAS_ITERATOR_DEBUGGING.md) to turn off the iterator debugging feature in a debug build. The following program does not assert, but still triggers undefined behavior.  
  
> [!IMPORTANT]
>  Use `_ITERATOR_DEBUG_LEVEL` to control `_HAS_ITERATOR_DEBUGGING`. For more information, see [_ITERATOR_DEBUG_LEVEL](../vs140/_ITERATOR_DEBUG_LEVEL.md).  
  
```cpp  
// iterator_debugging.cpp  
// compile with: /EHsc /MDd  
#define _HAS_ITERATOR_DEBUGGING 0  
#include <vector>  
#include <iostream>  
  
int main() {  
   std::vector<int> v ;  
  
   v.push_back(10);  
   v.push_back(15);  
   v.push_back(20);  
  
   std::vector<int>::iterator i = v.begin();  
   ++i;  
  
   std::vector<int>::iterator j = v.end();  
   --j;  
  
   std::cout<<*j<<'\n';  
  
   v.insert(i,25);   
  
   std::cout<<*j<<'\n'; // Using an old iterator after an insert  
}  
```  
  
 **20**  
**-572662307**   
## Example  
 An assert also occurs if you attempt to use an iterator before it is initialized, as shown here:  
  
```cpp  
/* compile with /EHsc /MDd */  
#include <string>  
using namespace std;  
int main() {  
   string::iterator i1, i2;  
   if (i1 == i2)  
      ;  
}  
```  
  
## Example  
 The following code example causes an assertion because the two iterators to the [for_each](../vs140/for_each.md) algorithm are incompatible. Algorithms check to determine whether the iterators that are supplied to them are referencing the same container.  
  
```cpp  
/* compile with /EHsc /MDd */  
#include <algorithm>  
#include <vector>  
using namespace std;  
  
int main()  
{  
    vector<int> v1;  
    vector<int> v2;  
  
    v1.push_back(10);  
    v1.push_back(20);  
  
    v2.push_back(10);  
    v2.push_back(20);  
  
    // The next line will assert because v1 and v2 are  
    // incompatible.  
    for_each(v1.begin(), v2.end(), [] (int& elem) { elem *= 2; } );  
}  
```  
  
 Notice that this example uses the lambda expression `[] (int& elem) { elem *= 2; }` instead of a functor. Although this choice has no bearing on the assert failure—a similar functor would cause the same failure—lambdas are a very useful way to accomplish compact function object tasks. For more information about lambda expressions, see [Lambda Expressions in C++](../vs140/Lambda-Expressions-in-C--.md).  
  
## Example  
 Debug iterator checking also causes an iterator variable that's declared in a `for` loop to be out of scope when the `for` loop scope ends.  
  
```cpp  
// debug_iterator.cpp  
// compile with: /EHsc /MDd  
#include <vector>  
#include <iostream>  
int main() {  
   std::vector<int> v ;  
  
   v.push_back(10);  
   v.push_back(15);  
   v.push_back(20);  
  
   for (std::vector<int>::iterator i = v.begin() ; i != v.end(); ++i)  
   ;  
   --i;   // C2065  
}  
```  
  
## Example  
 Debug iterators have non-trivial destructors. If a destructor does not run, for whatever reason, access violations and data corruption might occur. Consider this example:  
  
```cpp  
/* compile with: /EHsc /MDd */  
#include <vector>  
struct base {  
   // FIX: uncomment the next line  
   // virtual ~base() {}  
};  
  
struct derived : base {  
   std::vector<int>::iterator m_iter;  
   derived( std::vector<int>::iterator iter ) : m_iter( iter ) {}  
   ~derived() {}  
};  
  
int main() {  
   std::vector<int> vect( 10 );  
   base * pb = new derived( vect.begin() );  
   delete pb;  // doesn't call ~derived()  
   // access violation  
}  
```  
  
## See Also  
 [STL Overview](../vs140/C---Standard-Library-Overview.md)