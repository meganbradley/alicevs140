---
title: "CAnimationSize::operator="
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
ms.assetid: 6679e9dc-e861-44dd-b521-ce3e22605d5b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationSize::operator=
Assigns szSrc to CAnimationSize.  
  
## Syntax  
  
```  
void operator=(  
   const CSize& szSrc  
);  
```  
  
#### Parameters  
 `szSrc`  
 Refers to CSize or SIZE.  
  
## Remarks  
 Assigns szSrc to CAnimationSize. It's recommended to do that before animation start, because this operator calls SetDefaultValue, which recreates the underlying COM objects for Width and Height if they have been created. If you subscribed this animation object to events (ValueChanged or IntegerValueChanged), you need to re-enable these events.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationSize Class](../vs140/CAnimationSize-Class.md)