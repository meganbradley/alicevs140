---
title: "HString::MakeReference Method"
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
ms.topic: reference
ms.assetid: 9e1fd2b2-66ad-4a50-b647-a20ab10e522f
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HString::MakeReference Method
Creates an HStringReference object from a specified string parameter.  
  
## Syntax  
  
```  
template<unsigned int sizeDest>  
    static HStringReference MakeReference(  
              wchar_t const (&str)[ sizeDest]);  
  
    template<unsigned int sizeDest>  
    static HStringReference MakeReference(  
              wchar_t const (&str)[sizeDest],   
              unsigned int len);  
```  
  
#### Parameters  
 `sizeDest`  
 A template parameter that specifies the size of the destination HStringReference buffer.  
  
 `str`  
 A reference to a wide-character string.  
  
 `len`  
 The maximum length of the `str` parameter buffer to use in this operation. If the `len` parameter isn't specified, the entire `str` parameter is used.  
  
## Return Value  
 An HStringReference object whose value is the same as the specified `str` parameter.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [HString Class](../vs140/HString-Class.md)