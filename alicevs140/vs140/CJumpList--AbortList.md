---
title: "CJumpList::AbortList"
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
ms.assetid: 6e86a2af-5144-4bcd-96a6-44cd41372eb1
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CJumpList::AbortList
Aborts a list-building transaction without committing.  
  
## Syntax  
  
```  
void AbortList();  
```  
  
## Remarks  
 Calling this method has the same effect as destroying `CJumpList` without calling `CommitList`.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CJumpList](../vs140/CJumpList-Class.md)