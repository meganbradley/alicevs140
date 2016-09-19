---
title: "list::emplace"
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
ms.assetid: 26648a45-6402-4299-9682-516ebd089b44
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# list::emplace
Inserts an element constructed in place into a list at a specified position.  
  
## Syntax  
  
```  
  
      void emplace_back(  
   iterator _Where,  
   Type&& _Val  
);   
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`_Where`|The position in the target [list](../vs140/list-Class.md) where the first element is inserted.|  
|`_Val`|The element added to the end of the `list`.|  
  
## Remarks  
 If an exception is thrown, the `list` is left unaltered and the exception is rethrown.  
  
## Example  
  
```  
// list_emplace.cpp  
// compile with: /EHsc  
#include <list>  
#include <iostream>  
#include <string>  
  
int main( )   
{  
   using namespace std;  
   list <string> c2;  
   string str("a");  
  
   c2.emplace(c2.begin(), move( str ) );  
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