---
title: "CAnimationValue::CAnimationValue"
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
ms.assetid: ad772d92-0425-4232-b6a5-f056c3c8345b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationValue::CAnimationValue
Constructs a CAnimationValue object.  
  
## Syntax  
  
```  
CAnimationValue();  
CAnimationValue(  
   DOUBLE dblDefaultValue,  
   UINT32 nGroupID,  
   UINT32 nObjectID = (UINT32)-1,  
   DWORD dwUserData = 0  
);  
```  
  
#### Parameters  
 `dblDefaultValue`  
 Specifies default value.  
  
 `nGroupID`  
 Specifies Group ID.  
  
 `nObjectID`  
 Specifies Object ID.  
  
 `dwUserData`  
 specifies user-defined data.  
  
## Remarks  
 Constructs CAnimationValue object with default properties: default value, Group ID and Object ID are set to 0.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationValue Class](../vs140/CAnimationValue-Class.md)