---
title: "ios_base::precision"
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
ms.assetid: 7a358c50-6edc-4c5b-a744-2c42af85820c
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::precision
Specifies the number of digits to display in a floating-point number.  
  
## Syntax  
  
```  
  
      streamsize precision( ) const;   
streamsize precision(  
   streamsize _Prec  
);  
```  
  
#### Parameters  
 `_Prec`  
 The number of significant digits to display, or the number of digits after the decimal point in fixed notation.  
  
## Return Value  
 The first member function returns the stored [display precision](../vs140/ios_base-Class.md). The second member function stores `_Prec` in the display precision and returns its previous stored value.  
  
## Remarks  
 Floating-point numbers are displayed in fixed notation with [fixed](../vs140/fixed.md).  
  
## Example  
  
```  
// ios_base_precision.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   float i = 31.31234F;  
  
   cout.precision( 3 );  
   cout << i << endl;          // display three significant digits  
   cout << fixed << i << endl; // display three digits after decimal  
                               // point  
}  
```  
  
 **31.3**  
**31.312**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)