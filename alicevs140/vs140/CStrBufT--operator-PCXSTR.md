---
title: "CStrBufT::operator PCXSTR"
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
ms.assetid: 0c8f85a9-03dd-4abf-afdb-eb508c62edae
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStrBufT::operator PCXSTR
Directly accesses characters stored in the associated string object as a C-style string.  
  
## Syntax  
  
```  
  
operator PCXSTR( ) const throw( );  
  
```  
  
## Return Value  
 A character pointer to the string's data.  
  
## Remarks  
 Call this function to return a pointer to the character buffer of a string object. The contents of the string object cannot be changed with this pointer.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CStrBufT Class](../vs140/CStrBufT-Class.md)   
 [CStrBufT::operator PXSTR](../vs140/CStrBufT--operator-PXSTR.md)   
 [CStrBufT::PCXSTR](../vs140/CStrBufT--PCXSTR.md)