---
title: "CHandle::Detach"
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
ms.assetid: 0c048bb0-d9c2-4efe-9107-7720c214db67
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHandle::Detach
Call this method to detach a handle from a `CHandle` object.  
  
## Syntax  
  
```  
  
HANDLE Detach( ) throw( );  
  
```  
  
## Return Value  
 Returns the handle being detached.  
  
## Remarks  
 Releases ownership of the handle.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CHandle Class](../vs140/CHandle-Class.md)   
 [CHandle::Attach](../vs140/CHandle--Attach.md)