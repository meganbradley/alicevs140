---
title: "CMFCAutoHideButton::IsHorizontal"
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
ms.assetid: 5a5ec91b-8a0f-467d-b85b-b0a3df4ee5d0
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAutoHideButton::IsHorizontal
Determines whether the auto-hide button is horizontal or vertical.  
  
## Syntax  
  
```  
BOOL IsHorizontal() const;  
```  
  
## Return Value  
 Nonzero if the button is horizontal; 0 otherwise.  
  
## Remarks  
 The framework sets the orientation of a [CMFCAutoHideButton](../vs140/CMFCAutoHideButton-Class.md) object when you create it.  You can control the orientation by using the `dwAlignment` parameter in the [CMFCAutoHideButton::Create](../vs140/CMFCAutoHideButton--Create.md) method.  
  
## Requirements  
 **Header:** afxautohidebutton.h  
  
## See Also  
 [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)