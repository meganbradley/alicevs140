---
title: "CAnimationBaseObject::GetGroupID"
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
ms.assetid: 788c0e2b-3856-44c1-9dde-0d138bbccbc7
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::GetGroupID
Returns current Group ID.  
  
## Syntax  
  
```  
UINT32 GetGroupID() const;  
```  
  
## Return Value  
 Current Group ID.  
  
## Remarks  
 Use this method to retrieve Group ID. It's 0 if Group ID has not been set explicitly in constructor or with SetID.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)