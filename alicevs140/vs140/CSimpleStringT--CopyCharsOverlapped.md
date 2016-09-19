---
title: "CSimpleStringT::CopyCharsOverlapped"
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
ms.assetid: 1b76e655-2500-4edf-ab33-057de1d362c6
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::CopyCharsOverlapped
Copies a character or characters to a `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
      static void CopyCharsOverlapped(  
   XCHAR* pchDest,  
   const XCHAR* pchSrc,  
   int nChars   
) throw( );  
```  
  
#### Parameters  
 `pchDest`  
 A pointer to a character string.  
  
 `pchSrc`  
 A pointer to a string containing the characters to be copied.  
  
 `nChars`  
 The number of `pchSrc` characters to be copied.  
  
## Remarks  
 Call this method to copy characters from `pchSrc` to the `pchDest` string. Unlike `CopyChars`, `CopyCharsOverlapped` provides a safe method for copying from character buffers that might be overlapped.  
  
## Example  
 See the example for [CSimpleStringT::CopyChars](../vs140/CSimpleStringT--CopyChars.md), or the source code for `CSimpleStringT::SetString` (located in atlsimpstr.h).  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)