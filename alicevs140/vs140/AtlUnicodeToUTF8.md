---
title: "AtlUnicodeToUTF8"
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
ms.assetid: 104f13d8-379c-4bb0-b894-e54cad7ed9aa
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlUnicodeToUTF8
Call this function to convert a Unicode string to UTF-8.  
  
## Syntax  
  
```  
  
      ATL_NOINLINE inline int AtlUnicodeToUTF8(  
   LPCWSTR wszSrc,  
   int nSrc,  
   LPSTR szDest,  
   int nDest   
) throw( );  
```  
  
#### Parameters  
 *wszSrc*  
 The Unicode string to be converted  
  
 `nSrc`  
 The length in characters of the Unicode string.  
  
 `szDest`  
 Caller-allocated buffer to receive the converted string.  
  
 `nDest`  
 The length in bytes of the buffer.  
  
## Return Value  
 Returns the number of characters for the converted string.  
  
## Remarks  
 To determine the size of the buffer required for the converted string, call this function passing 0 for `szDest` and `nDest`.  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)