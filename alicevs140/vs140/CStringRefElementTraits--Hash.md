---
title: "CStringRefElementTraits::Hash"
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
ms.assetid: 4bf27480-98c8-4a97-a538-0c90be79b80e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringRefElementTraits::Hash
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
 [CStringRefElementTraits Class](../vs140/CStringRefElementTraits-Class.md)