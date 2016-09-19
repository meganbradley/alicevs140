---
title: "istreambuf_iterator::int_type"
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
ms.assetid: c345686a-b579-4f6e-b261-9c2a9cee1dad
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# istreambuf_iterator::int_type
A type that provides an integer type for an `istreambuf_iterator`.  
  
## Syntax  
  
```  
typedef typename traits_type::int_type int_type;  
```  
  
## Remarks  
 The type is a synonym for **Traits::int_type**.  
  
## Example  
  
```  
// istreambuf_iterator_int_type.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   istreambuf_iterator<char>::int_type inttype1 = 100;  
   cout << "The inttype1 = " << inttype1 << "." << endl;  
}  
```  
  
 **The inttype1 = 100.**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [istreambuf_iterator Class](../vs140/istreambuf_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)