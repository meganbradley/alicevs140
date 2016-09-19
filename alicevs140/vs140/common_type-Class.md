---
title: "common_type Class"
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
ms.assetid: 02bc4e7b-c63d-49de-9f8a-511d3a5c1e7f
caps.latest.revision: 22
translation.priority.mt: 
  - de-de
  - ja-jp
---
# common_type Class
Determines the common type of one or more types.  
  
## Syntax  
  
```  
  
template <class... T>  
   struct common_type;  
  
template <class T>  
   struct common_type< T> {  
      typedef typename decay< T>::type type;  
};  
  
template <class T, class U>  
   struct common_type< T, U> {  
      typedef typename decay< decltype(true ?  declval< T>() :  
         declval< U>())>::type type;  
};  
  
template <class T, class U, class... V>  
   struct common_type< T, U, V...> {  
      typedef typename common_type<typename common_type< T, U>::type, V...>::type type;  
};  
```  
  
#### Parameters  
 List of types that are either [complete types](../vs140/Incomplete-Types.md) or void.  
  
## Remarks  
 The `type` member is the common type to which all types in the parameter list can be converted.  
  
## Example  
 The following program demonstrates some correct usage scenarios and tests for results.  
  
```cpp  
// Compile using cl.exe /EHsc  
// common_type sample  
#include <iostream>  
#include <type_traits>  
  
struct Base {};  
struct Derived : Base {};  
  
int main()   
{  
    typedef std::common_type<unsigned char, short, int>::type NumericType;  
    typedef std::common_type<float, double>::type FloatType;  
    typedef std::common_type<const int, volatile int>::type ModifiedIntType;  
    typedef std::common_type<Base, Derived>::type ClassType;  
  
    std::cout << std::boolalpha;  
    std::cout << "Test for typedefs of common_type int" << std::endl;  
    std::cout << "NumericType: "     << std::is_same<int, NumericType>::value << std::endl;  
    std::cout << "FloatType: "       << std::is_same<int, FloatType>::value << std::endl;  
    std::cout << "ModifiedIntType: " << std::is_same<int, ModifiedIntType>::value << std::endl;  
    std::cout << "ClassType: "       << std::is_same<int, ClassType>::value << std::endl;  
    std::cout << "---------------------------" << std::endl;  
    std::cout << "Test for typedefs of common_type double" << std::endl;  
    std::cout << "NumericType: "     << std::is_same<double, NumericType>::value << std::endl;  
    std::cout << "FloatType: "       << std::is_same<double, FloatType>::value << std::endl;  
    std::cout << "ModifiedIntType: " << std::is_same<double, ModifiedIntType>::value << std::endl;  
    std::cout << "ClassType: "       << std::is_same<double, ClassType>::value << std::endl;  
    std::cout << "---------------------------" << std::endl;  
    std::cout << "Test for typedefs of common_type Base" << std::endl;  
    std::cout << "NumericType: "     << std::is_same<Base, NumericType>::value << std::endl;  
    std::cout << "FloatType: "       << std::is_same<Base, FloatType>::value << std::endl;  
    std::cout << "ModifiedIntType: " << std::is_same<Base, ModifiedIntType>::value << std::endl;  
    std::cout << "ClassType: "       << std::is_same<Base, ClassType>::value << std::endl;  
  
    return 0;  
}  
```  
  
## Output  
  
```  
Test for typedefs of common_type int  
NumericType: true  
FloatType: false  
ModifiedIntType: true  
ClassType: false  
---------------------------  
Test for typedefs of common_type double  
NumericType: false  
FloatType: true  
ModifiedIntType: false  
ClassType: false  
---------------------------  
Test for typedefs of common_type Base  
NumericType: false  
FloatType: false  
ModifiedIntType: false  
ClassType: true  
  
```  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)