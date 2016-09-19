---
title: "CAnimationBaseObject::GetObjectID"
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
ms.assetid: 8f46505d-50da-4cd1-b9be-6f8750f5026f
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::GetObjectID
Returns current Object ID.  
  
## Syntax  
  
```  
UINT32 GetObjectID() const;  
```  
  
## Return Value  
 Current Object ID.  
  
## Remarks  
 Use this method to retrieve Object ID. It's 0 if Object ID has not been set explicitly in constructor or with SetID.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)