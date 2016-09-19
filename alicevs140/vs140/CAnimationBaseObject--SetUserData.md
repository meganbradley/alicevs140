---
title: "CAnimationBaseObject::SetUserData"
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
ms.assetid: 34003d54-e35b-4493-bd2f-7c0bf5ae482c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::SetUserData
Sets user-defined data.  
  
## Syntax  
  
```  
void SetUserData (  
   DWORD dwUserData  
);  
```  
  
#### Parameters  
 `dwUserData`  
 Specifies the custom data.  
  
## Remarks  
 Use this method to associate a custom data with an animation object. This data may be retrieved later at runtime by GetUserData.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)