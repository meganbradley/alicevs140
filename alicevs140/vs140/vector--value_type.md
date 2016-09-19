---
title: "vector::value_type"
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
ms.assetid: 9316559a-a13f-4f4f-83e4-f926da4e8f7b
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# vector::value_type
A type that represents the data type stored in a vector.  
  
## Syntax  
  
```  
typedef typename Allocator::value_type value_type;  
```  
  
## Remarks  
 `value_type` is a synonym for the template parameter **Type**.  
  
## Example  
  
```  
// vector_value_type.cpp  
// compile with: /EHsc  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   vector<int>::value_type AnInt;  
   AnInt = 44;  
   cout << AnInt << endl;  
}  
```  
  
 **44**   
## Requirements  
 **Header:** <vector\>  
  
 **Namespace:** std  
  
## See Also  
 [vector Class](../vs140/vector-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)