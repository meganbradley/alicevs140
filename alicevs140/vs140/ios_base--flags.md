---
title: "ios_base::flags"
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
ms.assetid: 40efc25d-1b5f-46b8-a134-f3350cff8233
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::flags
Sets or returns the current flag settings.  
  
## Syntax  
  
```  
fmtflags flags( ) const;   
fmtflags flags(  
   fmtflags fmtfl  
);  
```  
  
#### Parameters  
 `fmtfl`  
 The new `fmtflags` setting.  
  
## Return Value  
 The previous or current `fmtflags` setting.  
  
## Remarks  
 See [ios_base::fmtflags](../vs140/ios_base--fmtflags.md) for a list of the flags.  
  
 The first member function returns the stored format flags. The second member function stores `fmtfl` in the format flags and returns its previous stored value.  
  
## Example  
  
```  
// ios_base_flags.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main ( )   
{  
   using namespace std;  
   cout << cout.flags( ) << endl;  
   cout.flags( ios::dec | ios::boolalpha );  
   cout << cout.flags( );  
}  
```  
  
 **513**  
**16896**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)