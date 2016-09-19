---
title: "set::clear"
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
ms.assetid: fd43fc55-65d2-49d9-be42-4265f81cb7eb
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::clear
Erases all the elements of a set.  
  
## Syntax  
  
```  
  
void clear( );  
  
```  
  
## Example  
  
```  
// set_clear.cpp  
// compile with: /EHsc  
#include <set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;     
   set <int> s1;  
  
   s1.insert( 1 );  
   s1.insert( 2 );  
  
   cout << "The size of the set is initially " << s1.size( )  
        << "." << endl;  
  
   s1.clear( );  
   cout << "The size of the set after clearing is "   
        << s1.size( ) << "." << endl;  
}  
```  
  
 **The size of the set is initially 2.**  
**The size of the set after clearing is 0.**   
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [set Class](../vs140/set-Class.md)   
 [set::empty and set::clear](../vs140/set--empty-and-set--clear.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)