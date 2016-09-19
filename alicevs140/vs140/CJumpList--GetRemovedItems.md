---
title: "CJumpList::GetRemovedItems"
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
ms.assetid: 2dfb7b29-3d00-4643-9bc8-f98b31edc3e9
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CJumpList::GetRemovedItems
Returns array of items that represent removed destinations.  
  
## Syntax  
  
```  
IObjectArray* GetRemovedItems();  
```  
  
## Return Value  
  
## Remarks  
 The removed destinations are retrieved during initialization of jump list. When generating a new destination list, applications are expected to first process the removed destinations list, clearing their tracking data for any item returned by the removed list enumerator. If an application attempts to provide an item that was just removed in the transaction that the current call to `BeginList` started, the method call that re-added that item will fail, to ensure that applications are respecting the removed list.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CJumpList](../vs140/CJumpList-Class.md)