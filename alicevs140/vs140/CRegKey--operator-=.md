---
title: "CRegKey::operator ="
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
ms.assetid: bb5dcbe3-3370-4b30-aafb-c46bc2d4ef3d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::operator =
Assignment operator.  
  
## Syntax  
  
```  
  
      CRegKey& operator =(  
   CRegKey& key   
) throw( );  
```  
  
#### Parameters  
 `key`  
 The key to copy.  
  
## Return Value  
 Returns a reference to the new key.  
  
## Remarks  
 This operator detaches `key` from its current object and assigns it to the `CRegKey` object instead.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)