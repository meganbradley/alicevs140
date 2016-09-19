---
title: "CUrl::operator ="
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
ms.assetid: ed70f55d-7519-452c-a986-f8b7c5515dd6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::operator =
Assigns the specified `CUrl` object to the current `CUrl` object.  
  
## Syntax  
  
```  
  
      CUrl & operator =(  
   const CUrl & urlThat   
) throw();  
```  
  
#### Parameters  
 `urlThat`  
 The `CUrl` object to copy into the current object.  
  
## Return Value  
 Returns a reference to the current object.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)