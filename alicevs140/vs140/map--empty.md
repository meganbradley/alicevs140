---
title: "map::empty"
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
ms.assetid: 6adafade-332e-4d6a-8925-510b8dee4f78
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# map::empty
Tests if a map is empty.  
  
## Syntax  
  
```  
  
bool empty( ) const;  
  
```  
  
## Return Value  
 **true** if the map is empty; **false** if the map is nonempty.  
  
## Example  
  
```  
// map_empty.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   map <int, int> m1, m2;  
  
   typedef pair <int, int> Int_Pair;  
   m1.insert ( Int_Pair ( 1, 1 ) );  
  
   if ( m1.empty( ) )  
      cout << "The map m1 is empty." << endl;  
   else  
      cout << "The map m1 is not empty." << endl;  
  
   if ( m2.empty( ) )  
      cout << "The map m2 is empty." << endl;  
   else  
      cout << "The map m2 is not empty." << endl;  
}  
```  
  
 **The map m1 is not empty.**  
**The map m2 is empty.**   
## Requirements  
 **Header:** <map\>  
  
 **Namespace:** std  
  
## See Also  
 [map Class](../vs140/map-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)