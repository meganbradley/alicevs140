---
title: "CSimpleStringT::GetLength"
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
ms.assetid: 1dd781f7-b3d7-441f-8fd6-7fd614c33c97
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::GetLength
Returns the number of characters in the `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
int GetLength( ) const throw( );  
  
```  
  
## Return Value  
 A count of the characters in the string.  
  
## Remarks  
 Call this method to return the number of characters in the object. The count does not include a null terminator.  
  
 For multibyte character sets (MBCS), `GetLength` counts each 8-bit character; that is, a lead and trail byte in one multibyte character are counted as two bytes. See [FreeExtra](../vs140/CSimpleStringT--FreeExtra.md) for an example of calling this function.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::IsEmpty](../vs140/CSimpleStringT--IsEmpty.md)