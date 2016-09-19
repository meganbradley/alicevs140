---
title: "tuple_element Class &lt;utility&gt;"
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
ms.assetid: f9db79e8-685c-49e3-97ee-81763e516ce3
caps.latest.revision: 20
translation.priority.mt: 
  - de-de
  - ja-jp
---
# tuple_element Class &lt;utility&gt;
Wraps the type of a `pair` element.  
  
## Syntax  
  
```  
// CLASS tuple_element (find element by index)  
template<size_t Index, class Tuple>  
struct tuple_element;  
  
// struct to determine type of element 0 in pair  
template<class Ty1, class Ty2>  
struct tuple_element<0, pair<Ty1, Ty2> >;  
  
// struct to determine type of element 1 in pair  
template<class Ty1, class Ty2>  
struct tuple_element<1, pair<Ty1, Ty2> >;  
  
// tuple_element for const  
template<size_t Index, class Tuple>  
struct tuple_element<Index, const Tuple>;  
  
// tuple_element for volatile  
template<size_t Index, class Tuple>  
struct tuple_element<Index, volatile Tuple>;  
  
// tuple_element for const volatile  
template<size_t Index, class Tuple>  
struct tuple_element<Index, const volatile Tuple>;  
  
template<size_t Index, class Tuple>  
using tuple_element_t = typename tuple_element<Index, Tuple>::type;  
```  
  
#### Parameters  
 Index  
 The position of the element; for pair this value is either 0 or 1.  
  
 `T1`  
 The type of the first pair element.  
  
 `T2`  
 The type of the second pair element.  
  
 type  
  
## Remarks  
 The templates are specializations of the template class [tuple_element](../vs140/tuple_element-Class--tuple-.md). Each has a single member typedef, `type`, which is a synonym for the type of the element at the specified position in the `pair`, with any const and/or volatile qualifications preserved. `tuple_element_t` is a convenient alias for `tuple_element<N, pair<T1, T2>>::type`. Use the [get Function <utility\>](../vs140/-utility--functions.md#get_function__lt_utility_gt_) to return the element at a specified position or (in C++14 / Visual Studio 2015) of a specified type.  
  
## Example  
  
```  
#include <utility>   
#include <iostream>   
  
using namespace std;  
  
typedef pair<int, double> MyPair;  
int main()  
{  
    MyPair c0(0, 1.333);  
  
    // display contents " 0 1"   
    cout << " " << get<0>(c0);  
    cout << " " << get<1>(c0) << endl;  
  
    // display first element " 0" by index  
    tuple_element<0, MyPair>::type val = get<0>(c0);  
    cout << " " << val;  
  
    // display second element by type   
    tuple_element<1, MyPair>::type val2 = get<double>(c0);  
    cout << " " << val2 << endl;  
}  
  
/*  
Output:  
0 1.333  
0 1.333  
*/  
```  
  
## Requirements  
 **Header:** <utility\>  
  
 **Namespace:** std  
  
## See Also  
 [<utility\>](../vs140/-utility-.md)   
 [get](../vs140/-utility--functions.md#get_function__lt_utility_gt_)   
 [tuple_size](../vs140/tuple_size-Class--utility-.md)