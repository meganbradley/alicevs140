---
title: "list::value_type"
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
ms.assetid: 7f7a9fda-ed6f-45c8-adb7-e8586e43c2f2
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::value_type
A type that represents the data type stored in a list.  
  
## Syntax  
  
```  
typedef typename Allocator::value_type value_type;  
```  
  
## Remarks  
 `value_type` is a synonym for the template parameter **Type**.  
  
## Example  
  
```  
// list_value_type.cpp  
// compile with: /EHsc  
#include <list>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   list<int>::value_type AnInt;  
   AnInt = 44;  
   cout << AnInt << endl;  
}  
```  
  
 **44**   
## Requirements  
 **Header:** <list\>  
  
 **Namespace:** std  
  
## See Also  
 [list Class](../vs140/list-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)