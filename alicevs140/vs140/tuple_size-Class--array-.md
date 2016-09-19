---
title: "tuple_size Class &lt;array&gt;"
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
ms.assetid: ef95ffee-59b4-4396-817f-487d4486772d
caps.latest.revision: 21
translation.priority.mt: 
  - de-de
  - ja-jp
---
# tuple_size Class &lt;array&gt;
Wraps the size of an array.  
  
## Syntax  
  
```  
template<class Tuple>  
struct tuple_size;  
  
// struct to determine number of elements in array  
template<class T, size_t Size>  
struct tuple_size<array<T, Size> >  
: integral_constant<size_t, Size>;  
  
// size of const tuple  
template<class Tuple>  
struct tuple_size<const Tuple>;  
  
// size of volatile tuple  
template<class Tuple>  
struct tuple_size<volatile Tuple>;  
  
// size of const volatile tuple  
template<class Tuple>  
struct tuple_size<const volatile Tuple>;  
  
```  
  
## Template Parameters  
 `T`  
 The type of an element.  
  
 `Size`  
 The size of the array.  
  
## Remarks  
 This template is a specialization of the template class [tuple_size](../vs140/tuple_size-Class--tuple-.md). It has a member `value` that is an integral constant expression whose value is `N`, which is the size of the array.  
  
## Example  
  
```  
#include <array>   
#include <iostream>   
  
using namespace std;  
  
typedef array<int, 4> MyArray;  
  
int main()  
{  
    MyArray c0 { 0, 1, 2, 3 };  
  
    // display contents " 0 1 2 3"   
    for (const auto& e : c0)  
    {  
        cout << e;  
    }  
    cout << endl;  
  
    // display size " 4"   
    cout << " " << tuple_size<MyArray>::value << endl;  
}  
/*  
Output:  
0123  
4  
*/  
  
```  
  
## Requirements  
 **Header:** <array\>  
  
 **Namespace:** std  
  
## See Also  
 [<array\>](../vs140/-array-.md)   
 [<tuple\>](../vs140/-tuple-.md)   
 [tuple_size](../vs140/tuple_size-Class--tuple-.md)