---
title: "map::max_size"
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
ms.assetid: f036ef05-c0e0-4a90-9388-9a2610959df6
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# map::max_size
Returns the maximum length of the map.  
  
## Syntax  
  
```  
  
size_type max_size( ) const;  
  
```  
  
## Return Value  
 The maximum possible length of the map.  
  
## Example  
  
```  
// map_max_size.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   map <int, int> m1;  
   map <int, int> :: size_type i;  
  
   i = m1.max_size( );  
   cout << "The maximum possible length "  
        << "of the map is " << i << "."  
        << endl << "(Magnitude is machine specific.)";  
}  
```  
  
## Sample Output  
 The following output is for x86.  
  
```  
The maximum possible length of the map is 536870911.  
(Magnitude is machine specific.)  
```  
  
## Requirements  
 **Header:** <map\>  
  
 **Namespace:** std  
  
## See Also  
 [map Class](../vs140/map-Class.md)   
 [map::max_size, map::clear, map::erase, and map::size](../vs140/map--max_size--map--clear--map--erase--and-map--size.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)