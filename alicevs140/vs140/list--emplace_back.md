---
title: "list::emplace_back"
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
ms.assetid: 8768150a-3d3a-4a6f-8dd6-d381f48ae532
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::emplace_back
Adds an element constructed in place to the beginning of a list.  
  
## Syntax  
  
```  
  
      void emplace_back(  
   Type&& _Val  
);   
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`_Val`|The element added to the end of the [list](../vs140/list-Class.md).|  
  
## Remarks  
 If an exception is thrown, the `list` is left unaltered and the exception is rethrown.  
  
## Example  
  
```  
// list_emplace_back.cpp  
// compile with: /EHsc  
#include <list>  
#include <iostream>  
#include <string>  
  
int main( )   
{  
   using namespace std;  
   list <string> c2;  
   string str("a");  
  
   c2.emplace_back( move( str ) );  
   cout << "Moved first element: " << c2.back( ) << endl;  
}  
```  
  
 **Moved first element: a**   
## Requirements  
 **Header:** <list\>  
  
 **Namespace:** std  
  
## See Also  
 [list Class](../vs140/list-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)