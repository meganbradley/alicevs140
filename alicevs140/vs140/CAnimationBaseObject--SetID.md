---
title: "CAnimationBaseObject::SetID"
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
ms.assetid: 4cc98be2-65df-466c-807e-f875076fe0fb
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::SetID
Sets new IDs.  
  
## Syntax  
  
```  
void SetID(  
   UINT32 nObjectID,  
   UINT32 nGroupID = 0  
);  
```  
  
#### Parameters  
 `nObjectID`  
 Specifies new Object ID.  
  
 `nGroupID`  
 Specifies new Group ID.  
  
## Remarks  
 Allows to change Object ID and Group ID. If the new Group ID differs from the current ID, an animation object is moved to another group (a new group will be created, if necessary).  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)