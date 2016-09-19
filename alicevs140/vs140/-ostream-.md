---
title: "&lt;ostream&gt;"
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
ms.assetid: 90c3b6fb-57cd-4ae7-99b8-8512f24a67d2
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;ostream&gt;
Defines the template class [basic_ostream](../vs140/basic_ostream-Class.md), which mediates insertions for the iostreams. The header also defines several related manipulators. (This header is typically included for you by another of the iostreams headers. You rarely need to include it directly.)  
  
## Syntax  
  
```  
#include <ostream>  
  
```  
  
### Typedefs  
  
|||  
|-|-|  
|[ostream](../vs140/-ostream--typedefs.md#ostream)|Creates a type from `basic_ostream` that is specialized on `char` and `char_traits` specialized on `char`.|  
|[wostream](../vs140/-ostream--typedefs.md#wostream)|Creates a type from `basic_ostream` that is specialized on `wchar_t` and `char_traits` specialized on `wchar_t`.|  
  
### Manipulators  
  
|||  
|-|-|  
|[endl](../vs140/-ostream--functions.md#endl)|Terminates a line and flushes the buffer.|  
|[ends](../vs140/-ostream--functions.md#ends)|Terminates a string.|  
|[flush](../vs140/-ostream--functions.md#flush)|Flushes the buffer.|  
|[swap](../vs140/-ostream--functions.md#swap)|Exchanges the values of the left `basic_ostream` object parameter for those of the right `basic_ostream` object parameter.|  
  
### Operators  
  
|||  
|-|-|  
|[operator<<](../vs140/-ostream--operators.md#operator_lt__lt_)|Writes various types to the stream.|  
  
### Classes  
  
|||  
|-|-|  
|[basic_ostream](../vs140/basic_ostream-Class.md)|The template class describes an object that controls insertion of elements and encoded objects into a stream buffer.|  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)