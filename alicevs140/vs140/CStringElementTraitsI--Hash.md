---
title: "CStringElementTraitsI::Hash"
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
ms.assetid: d38c73a5-031f-405b-959c-f4fec581b5f2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringElementTraitsI::Hash
Call this static function to calculate a hash value for the given string element.  
  
## Syntax  
  
```  
  
      static ULONG Hash(  
   INARGTYPE str   
) throw( );  
```  
  
#### Parameters  
 `str`  
 The string element.  
  
## Return Value  
 Returns a hash value, calculated using the string's contents.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CStringElementTraitsI Class](../vs140/CStringElementTraitsI-Class.md)   
 [CStringElementTraits::Hash](../vs140/CStringElementTraits--Hash.md)