---
title: "AtlIsUnsafeUrlChar"
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
ms.assetid: bf434973-0530-48ea-86cc-f40551e4d4a3
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlIsUnsafeUrlChar
Call this function to find out whether a character is safe for use in a URL.  
  
## Syntax  
  
```  
  
      inline BOOL AtlIsUnsafeUrlChar(  
   char chIn   
) throw( );  
```  
  
#### Parameters  
 `chIn`  
 The character to be tested for safety.  
  
## Return Value  
 Returns **TRUE** if the input character is unsafe, **FALSE** otherwise.  
  
## Remarks  
 Characters that should not be used in URLs can be tested using this function and converted using [AtlCanonicalizeUrl](../vs140/AtlCanonicalizeUrl.md).  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)