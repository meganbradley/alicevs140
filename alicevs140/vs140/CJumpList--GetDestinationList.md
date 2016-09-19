---
title: "CJumpList::GetDestinationList"
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
ms.assetid: 66ca85bd-1f79-4201-a660-1e6db5919282
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CJumpList::GetDestinationList
Retrieves an interface pointer to destination list.  
  
## Syntax  
  
```  
ICustomDestinationList* GetDestinationList();  
```  
  
## Return Value  
  
## Remarks  
 If the jump list has not been initialized, or has been committed or aborted, the returned value will be `NULL`.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CJumpList](../vs140/CJumpList-Class.md)