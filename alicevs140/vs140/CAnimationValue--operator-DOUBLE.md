---
title: "CAnimationValue::operator DOUBLE"
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
ms.assetid: d872dd98-8f12-4b5c-84d4-a177904b02df
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationValue::operator DOUBLE
Provides conversion between CAnimationValue and DOUBLE.  
  
## Syntax  
  
```  
operator DOUBLE();  
```  
  
## Return Value  
 Current value of Animation Value.  
  
## Remarks  
 Provides conversion between CAnimationValue and DOUBLE. This method internally calls GetValue and doesn't check for errors. If GetValue fails, the returned value will contain a default value previously set in constructor or with SetDefaultValue.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationValue Class](../vs140/CAnimationValue-Class.md)