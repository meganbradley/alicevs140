---
title: "CAnimationRect::GetValue"
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
ms.assetid: 6c5d747d-9c2a-4137-bb26-d570baca015b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationRect::GetValue
Returns current value.  
  
## Syntax  
  
```  
BOOL GetValue(  
   CRect& rect  
);  
```  
  
#### Parameters  
 `rect`  
 Output. Contains the current value when this method returns.  
  
## Return Value  
 TRUE, if the current value was successfully retrieved; otherwise FALSE.  
  
## Remarks  
 Call this function to retrieve the current value of animation rectangle. If this method fails or underlying COM objects for left, top, right and bottom have not been initialized, rect contains default value, which was previously set in constructor or by SetDefaultValue.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationRect Class](../vs140/CAnimationRect-Class.md)