---
title: "CAnimationPoint::CAnimationPoint"
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
ms.assetid: 973206d3-99e7-475b-8786-c90b35ad556c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationPoint::CAnimationPoint
Constructs CAnimationPoint object.  
  
## Syntax  
  
```  
CAnimationPoint();  
CAnimationPoint(  
   const CPoint& ptDefault,  
   UINT32 nGroupID,  
   UINT32 nObjectID = (UINT32)-1,  
   DWORD dwUserData = 0  
);  
```  
  
#### Parameters  
 `ptDefault`  
 Specifies default point coordinates.  
  
 `nGroupID`  
 Specifies Group ID.  
  
 `nObjectID`  
 Specifies Object ID.  
  
 `dwUserData`  
 Specifies user-defined data.  
  
## Remarks  
 Constructs CAnimationPoint object with default properties: default point coordinates, Group ID and Object ID are set to 0.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationPoint Class](../vs140/CAnimationPoint-Class.md)