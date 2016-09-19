---
title: "set::reference"
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
ms.assetid: 2fb13b84-b436-4c59-bd69-a530fd330737
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::reference
A type that provides a reference to an element stored in a set.  
  
## Syntax  
  
```  
typedef typename allocator_type::reference reference;  
```  
  
## Example  
  
```  
// set_reference.cpp  
// compile with: /EHsc  
#include <set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   set <int> s1;  
  
   s1.insert( 10 );  
   s1.insert( 20 );  
  
   // Declare and initialize a reference &Ref1 to the 1st element  
   const int &Ref1 = *s1.begin( );  
  
   cout << "The first element in the set is "  
        << Ref1 << "." << endl;  
}  
```  
  
 **The first element in the set is 10.**   
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [set Class](../vs140/set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)