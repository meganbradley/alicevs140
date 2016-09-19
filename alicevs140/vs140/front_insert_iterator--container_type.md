---
title: "front_insert_iterator::container_type"
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
ms.assetid: 4769a767-746c-44be-a457-20893f2bd4b0
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# front_insert_iterator::container_type
A type that represents the container into which a front insertion is to be made.  
  
## Syntax  
  
```  
  
typedef Container container_type;  
  
```  
  
## Remarks  
 The type is a synonym for the template parameter **Container**.  
  
## Example  
  
```  
// front_insert_iterator_container_type.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <list>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   list<int> L1;  
   front_insert_iterator<list<int> >::container_type L2 = L1;  
   front_inserter ( L2 ) = 20;  
   front_inserter ( L2 ) = 10;  
   front_inserter ( L2 ) = 40;  
  
   list <int>::iterator vIter;  
   cout << "The list L2 is: ( ";  
   for ( vIter = L2.begin ( ) ; vIter != L2.end ( ); vIter++)  
      cout << *vIter << " ";  
   cout << ")." << endl;  
}  
```  
  
 **The list L2 is: ( 40 10 20 ).**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [front_insert_iterator Class](../vs140/front_insert_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)