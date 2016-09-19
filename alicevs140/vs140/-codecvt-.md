---
title: "&lt;codecvt&gt;"
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
ms.assetid: d44ee229-00d5-4761-9b48-0c702122789d
caps.latest.revision: 21
translation.priority.mt: 
  - de-de
  - ja-jp
---
# &lt;codecvt&gt;
Defines several template classes that describe objects based on template class [codecvt](../vs140/codecvt-Class.md). These objects can serve as [locale facets](../vs140/locale-Class.md#facet_class) that control conversions between a sequence of values of type `Elem` and a sequence of values of type `char`.  
  
## Syntax  
  
```  
#include <codecvt>  
  
```  
  
## Remarks  
 The locale facets declared in this header convert between several character encodings. For wide characters (stored within the program in fixed-size integers):  
  
-   UCS-4 is Unicode (ISO 10646) encoded within the program  
  
-   UCS-4 is Unicode (ISO 10646) encoded within the program as a 32-bit integer.  
  
-   UCS-2 is Unicode encoded within the program  
  
-   UCS-2 is Unicode encoded within the program as a 16-bit integer.  
  
-   UTF-16 is Unicode encoded within the program as either one  
  
-   UTF-16 is Unicode encoded within the program as either one or two 16-bit integers. (Note that this does not meet all the requirements of a valid wide-character encoding for Standard C or Standard C++. Nevertheless it is widely used as such.)  
  
 For byte streams (stored in a file, transmitted as a byte sequence, or stored within the program in an array of `char`):  
  
-   UTF-8 is Unicode encoded  
  
-   UTF-8 is Unicode encoded within a byte stream as one or more eight-bit bytes with a deterministic byte order.  
  
-   UTF-16LE is Unicode encoded  
  
-   UTF-16LE is Unicode encoded within a byte stream as UTF-16 with each 16-bit integer presented as two eight-bit bytes, less significant byte first.  
  
-   UTF-16BE is Unicode encoded  
  
-   UTF-16BE is Unicode encoded within a byte stream as UTF-16 with each 16-bit integer presented as two eight-bit bytes, more significant byte first.  
  
### Enumerations  
  
|||  
|-|-|  
|[codecvt_mode](../vs140/-codecvt--enums.md#codecvt_mode_enumeration)|Specifies configuration information for locale facets.|  
  
### Classes  
  
|||  
|-|-|  
|[codecvt_utf8](../vs140/codecvt_utf8.md)|Represents a locale facet that converts between wide characters encoded as UCS-2 or UCS-4, and a byte stream encoded as UTF-8.|  
|[codecvt_utf8_utf16](../vs140/codecvt_utf8_utf16.md)|Represents a locale facet that converts between wide characters encoded as UTF-16 and a byte stream encoded as UTF-8.|  
|[codecvt_utf16](../vs140/codecvt_utf16.md)|Represents a locale facet that converts between wide characters encoded as UCS-2 or UCS-4 and a byte stream encoded as UTF-16LE or UTF-16BE.|  
  
## Requirements  
 **Header:** <codecvt\>  
  
 **Namespace:** stdt  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)