---
title: "CJumpList::InitializeList"
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
ms.assetid: a8aff2e3-adeb-4ba3-8f24-4c311b5a5abc
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CJumpList::InitializeList
Begins a list-building transaction.  
  
## Syntax  
  
```  
BOOL InitializeList();  
```  
  
## Return Value  
  
## Remarks  
 You don't need to call this method explicitly unless you wish to retrieve a pointer to `ICustomDestinationList` using `GetDestinationList`, the number of available slots using `GetMaxSlots`, or list of removed items using `GetRemovedItems`.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CJumpList](../vs140/CJumpList-Class.md)