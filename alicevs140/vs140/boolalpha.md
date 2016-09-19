---
title: "boolalpha"
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
ms.assetid: 61930ce9-e40e-4837-a299-ab23984ca2ac
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# boolalpha
Specifies that variables of type [bool](../vs140/bool--C---.md) appear as **true** or **false** in the stream.  
  
## Syntax  
  
```  
  
      ios  
      _  
      base& boolalpha(  
   ios_base& _Str  
);  
```  
  
#### Parameters  
 `_Str`  
 A reference to an object of type [ios_base](../vs140/ios_base-Class.md), or to a type that inherits from `ios_base`.  
  
## Return Value  
 A reference to the object from which _*Str* is derived.  
  
## Remarks  
 By default, variables of type `bool` are displayed as 1 or 0.  
  
 `boolalpha` effectively calls `_Str.`[setf](../vs140/ios_base--setf.md)(`ios_base::boolalpha`), and then returns `_Str.`  
  
 [noboolalpha](../vs140/noboolalpha.md) reverses the effect of `boolalpha`.  
  
## Example  
  
```  
// ios_boolalpha.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   bool b = true;  
   cout << b << endl;  
   boolalpha( cout );  
   cout << b << endl;  
   noboolalpha( cout );  
   cout << b << endl;  
   cout << boolalpha << b << endl;  
}  
```  
  
 **1**  
**true**  
**1**  
**true**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)