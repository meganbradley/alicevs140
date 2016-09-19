---
title: "dec"
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
ms.assetid: c8045c76-e259-4ce1-96c0-f7b8c0b57c0d
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# dec
Specifies that integer variables appear in base 10 notation.  
  
## Syntax  
  
```  
  
      ios  
      _  
      base& dec(  
   ios_base& _Str  
);  
```  
  
#### Parameters  
 `_Str`  
 A reference to an object of type [ios_base](../vs140/ios_base-Class.md), or to a type that inherits from `ios_base`.  
  
## Return Value  
 A reference to the object from which _*Str* is derived.  
  
## Remarks  
 By default, integer variables are displayed in base 10.  
  
 **dec** effectively calls `_Str``.`[setf](../vs140/ios_base--setf.md)(`ios_base::dec`**, ios_base::basefield**), and then returns `_Str`.  
  
## Example  
  
```  
// ios_dec.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   int i = 100;  
  
   cout << i << endl;   // Default is base 10  
   cout << hex << i << endl;     
   dec( cout );  
   cout << i << endl;  
   oct( cout );  
   cout << i << endl;  
   cout << dec << i << endl;  
}  
```  
  
 **100**  
**64**  
**100**  
**144**  
**100**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)