---
title: "CAnimationBaseObject::CAnimationBaseObject"
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
ms.assetid: da0918e9-df9d-4a8f-9579-4604ede99203
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::CAnimationBaseObject
Constructs an animation object.  
  
## Syntax  
  
```  
CAnimationBaseObject();  
CAnimationBaseObject(  
   UINT32 nGroupID,  
   UINT32 nObjectID = (UINT32)-1,  
   DWORD dwUserData = 0  
);  
```  
  
#### Parameters  
 `nGroupID`  
 Specifies Group ID.  
  
 `nObjectID`  
 Specifies Object ID.  
  
 `dwUserData`  
 User-defined data, which can be associated with animation object and retrieved later at runtime.  
  
## Remarks  
 Constructs an animation objects and assigns default Object ID (0) and Group ID (0).  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)