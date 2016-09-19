---
title: "CStringElementTraits::Hash"
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
ms.assetid: 87ecfe7b-d818-4cf9-ab97-cd5429fb4a6b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringElementTraits::Hash
Call this static function to calculate a hash value for the given string element.  
  
## Syntax  
  
```  
  
      static ULONG Hash(  
   INARGTYPE str   
);  
```  
  
#### Parameters  
 `str`  
 The string element.  
  
## Return Value  
 Returns a hash value, calculated using the string's contents.  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringElementTraits Class](../vs140/CStringElementTraits-Class.md)   
 [CStringElementTraitsI::Hash](../vs140/CStringElementTraitsI--Hash.md)