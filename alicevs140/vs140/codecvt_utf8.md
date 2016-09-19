---
title: "codecvt_utf8"
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
ms.assetid: 2a87478f-e2d4-4b8d-ad9c-00add01d1bb0
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# codecvt_utf8
Represents a [locale](../vs140/locale-Class.md) facet that converts between wide characters encoded as UCS-2 or UCS-4, and a byte stream encoded as UTF-8.  
  
## Syntax  
  
```  
template<  
    class Elem,  
    unsigned long Maxcode = 0x10ffff,  
    codecvt_mode Mode = (codecvt_mode)0  
>  
class codecvt_utf8 : public std::codecvt<Elem, char, StateType>  
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