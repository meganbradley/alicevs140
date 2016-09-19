---
title: "CAnimationBaseObject::GetUserData"
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
ms.assetid: 622ce40c-ea59-4c69-970f-a89d26903390
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::GetUserData
Returns user defined data.  
  
## Syntax  
  
```  
DWORD GetUserData() const;  
```  
  
## Return Value  
 A value of custom data.  
  
## Remarks  
 Call this method to retrieve the custom data at runtime. The returned value will be 0 if it was not explicitly initialized in constructor or with SetUserData.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)