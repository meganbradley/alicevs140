---
title: "&lt;ctgmath&gt;"
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
ms.assetid: ff521893-f445-4dc8-a2f6-699185bb7024
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;ctgmath&gt;
In effect, includes the Standard C++ library headers <ccomplex\> and <cmath\>, which provide type-generic math macros equivalent to <tgmath.h>.  
  
## Syntax  
  
```  
#include <ctgmath>  
  
```  
  
## Remarks  
 The functionality of the Standard C library header <tgmath.h> is provided by overloads in <ccomplex\> and <cmath\>.  
  
 Including this header ensures that the names declared using external linkage in the Standard C library header are declared in the `std` namespace.  
  
## See Also  
 [<ccomplex\>](../vs140/-ccomplex-.md)   
 [<cmath\>](../vs140/-cmath-.md)   
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [Standard C++ Library Overview](../vs140/C---Standard-Library-Overview.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)