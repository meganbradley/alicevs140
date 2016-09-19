---
title: "&lt;array&gt; functions"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e0700a33-a833-4655-8735-16e71175efc8
caps.latest.revision: 10
---
# &lt;array&gt; functions
|||  
|-|-|  
|[get Function](#get_function)|[swap Function](#swap_function)|  
  
##  <a name="get_function"></a>  get Function  
 Returns a reference to `arr[Index]`.  
  
```  
  
template<int Index, class T, size_t N>  
constexpr T& get(array<T, N>& arr) noexcept;  
  
template<int Index, class T, size_t N>  
constexpr const T& get(const array<T, N>& arr) noexcept;  
  
template<int Index, class T, size_t N>  
constexpr T&& get(array<T, N>&& arr) noexcept;  
```  
  
### Parameters  
 `Index`  
 The element offset.  
  
 `T`  
 The type of an element.  
  
 `N`  
 The number of elements in the array.  
  
 `arr`  
 The array to select from.  
  
### Example  
  
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
        cout << " " << e;  
    }  
    cout << endl;  
  
    // display odd elements " 1 3"   
    cout << " " << get<1>(c0);  
    cout << " " << get<3>(c0) << endl;  
}  
  
/*  
Output:  
0 1 2 3  
1 3  
*/  
```  
  
##  <a name="swap_function"></a>  swap Function  
 Swaps two arrays.  
  
```  
template<class Ty, std::size_t N>  
    void swap(  
        array<Ty, N>& left,  
        array<Ty, N>& right);  
```  
  
### Parameters  
 `Ty`  
 The type of an element.  
  
 `N`  
 The size of the array.  
  
 `left`  
 The first array to swap.  
  
 `right`  
 The second array to swap.  
  
### Remarks  
 The template function executes `left`. `swap(``right``)`.  
  
### Example  
  
```  
// std_tr1__array__swap.cpp   
// compile with: /EHsc   
#include <array>   
#include <iostream>   
  
typedef std::array<int, 4> Myarray;   
int main()   
    {   
    Myarray c0 = {0, 1, 2, 3};   
  
// display contents " 0 1 2 3"   
    for (Myarray::const_iterator it = c0.begin();   
        it != c0.end(); ++it)   
        std::cout << " " << *it;   
    std::cout << std::endl;   
  
    Myarray c1 = {4, 5, 6, 7};   
    c0.swap(c1);   
  
// display swapped contents " 4 5 6 7"   
    for (Myarray::const_iterator it = c0.begin();   
        it != c0.end(); ++it)   
        std::cout << " " << *it;   
    std::cout << std::endl;   
  
    swap(c0, c1);   
  
// display swapped contents " 0 1 2 3"   
    for (Myarray::const_iterator it = c0.begin();   
        it != c0.end(); ++it)   
        std::cout << " " << *it;   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
   **0 1 2 3**  
 **4 5 6 7**  
 **0 1 2 3**    
## See Also  
 [&lt;array&gt;](../vs140/-array-.md)