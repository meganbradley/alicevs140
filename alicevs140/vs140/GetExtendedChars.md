---
title: "GetExtendedChars"
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
ms.assetid: 26c5fa33-f313-4c4b-baf7-cca2ac11885c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetExtendedChars
Call this function to get the number of extended characters in a string.  
  
## Syntax  
  
```  
  
      inline int GetExtendedChars(  
   LPCSTR szSrc,  
   int nSrcLen   
) throw( );  
```  
  
#### Parameters  
 `szSrc`  
 The string to be analyzed.  
  
 `nSrcLen`  
 The length of the string in characters.  
  
## Return Value  
 Returns the number of extended characters found within the string as determined by [IsExtendedChar](../vs140/IsExtendedChar.md).  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [IsExtendedChar](../vs140/IsExtendedChar.md)