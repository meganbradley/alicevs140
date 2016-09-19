---
title: "get Function &lt;tuple&gt;"
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
ms.assetid: 9d6c9820-3f79-4649-8cd8-1f9f78a0839e
caps.latest.revision: 23
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# get Function &lt;tuple&gt;
Gets an element from a `tuple` object, by index or (in C++14) by type.  
  
## Syntax  
  
```  
  
// by index:// get reference to Index element of tupletemplate<size_t Index, class... Types> constexpr tuple_element_t<Index, tuple<Types...>> &    get(tuple<Types...>& Tuple) noexcept;// get const reference to Index element of tupletemplate<size_t Index, class... Types> constexpr const tuple_element_t<Index, tuple<Types...>> &    get(const tuple<Types...>& Tuple) noexcept;// get rvalue reference to Index element of tupletemplate<size_t Index, class... Types> constexpr tuple_element_t<Index, tuple<Types...>> &&    get(tuple<Types...>&& Tuple) noexcept;// (C++14) by type:// get reference to T element of tupletemplate<class T, class... Types> constexpr T& get(tuple<Types...>& Tuple) noexcept;// get const reference to T element of tupletemplate<class T, class... Types> constexpr const T& get(const tuple<Types...>& Tuple) noexcept;// get rvalue reference to T element of tupletemplate<class T, class... Types> constexpr T&& get(tuple<Types...>&& Tuple) noexcept;  
  
```  
  
#### Parameters  
 `Index`  
 The index of the element to get.  
  
 `Types`  
 The sequence of types declared in the tuple, in declaration order.  
  
 `T`  
 The type of the element to get.  
  
 `Tuple`  
 A std::tuple that contains any number of elements.  
  
## Remarks  
 The template functions return a reference to the value at index `Index`, or of type `T` in the `tuple` object.  
  
 Calling `get<T>(Tuple)` will produce a compiler error if Tuple contains more or less than one element of type T.  
  
## Example  
  
```  
#include <tuple>   
#include <iostream>   
#include <string>  
  
using namespace std;  
  
int main()  
{  
    tuple<int, double, string> tup(0, 1.42, "Call me Tuple");  
  
    // get elements by index  
    cout << " " << get<0>(tup);  
    cout << " " << get<1>(tup);  
    cout << " " << get<2>(tup) << endl;  
  
    // get elements by type  
    cout << " " << get<int>(tup);  
    cout << " " << get<double>(tup);  
    cout << " " << get<string>(tup) << endl;  
  
}  
  
/*  
Output:  
0 1.42 Call me Tuple  
0 1.42 Call me Tuple  
*/  
  
```  
  
## Requirements  
 **Header:** <tuple\>  
  
 **Namespace:** std  
  
## See Also  
 [<tuple\>](../vs140/-tuple-.md)   
 [tuple_element](../vs140/tuple_element-Class--tuple-.md)