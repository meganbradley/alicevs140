---
title: "codecvt_utf8_utf16"
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
ms.assetid: 4c12c881-5dba-4e39-b338-0b9caff5af29
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# codecvt_utf8_utf16
Represents a [locale](../vs140/locale-Class.md) facet that converts between wide characters encoded as UTF-16 and a byte stream encoded as UTF-8.  
  
## Syntax  
  
```  
template<  
    class Elem,  
    unsigned long Maxcode = 0x10ffff,  
    codecvt_mode Mode = (codecvt_mode)0  
>  
class codecvt_utf8_utf16 : public _STD codecvt<Elem, char, StateType>  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Elem`|The wide-character element type.|  
|`Maxcode`|The maximum number of characters for the locale facet.|  
|`Mode`|Configuration information for the locale facet.|  
  
## Remarks  
 The byte stream can be written to either a binary file or a text file.  
  
## Requirements  
 **Header:** <codecvt\>  
  
 **Namespace:** std