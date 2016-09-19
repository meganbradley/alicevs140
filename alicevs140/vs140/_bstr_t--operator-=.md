---
title: "_bstr_t::operator ="
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
ms.topic: language-reference
ms.assetid: fb31bb1b-ce29-4388-b5fd-8dac830cf18a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _bstr_t::operator =
**Microsoft Specific**  
  
 Assigns a new value to an existing `_bstr_t` object.  
  
## Syntax  
  
```  
  
      _bstr_t& operator=(  
   const _bstr_t& s1   
) throw ( );  
_bstr_t& operator=(  
   const char* s2   
);  
_bstr_t& operator=(  
   const wchar_t* s3   
);  
_bstr_t& operator=(  
   const _variant_t& var   
);  
```  
  
#### Parameters  
 *s1*  
 A `_bstr_t` object to be assigned to an existing `_bstr_t` object.  
  
 *s2*  
 A multibyte string to be assigned to an existing `_bstr_t` object.  
  
 `s3`  
 A Unicode string to be assigned to an existing `_bstr_t` object.  
  
 `var`  
 A `_variant_t` object to be assigned to an existing `_bstr_t` object.  
  
 **END Microsoft Specific**  
  
## Example  
 See [_bstr_t::Assign](../vs140/_bstr_t--Assign.md) for an example of using `operator=`.  
  
## See Also  
 [_bstr_t Class](../vs140/_bstr_t-Class.md)