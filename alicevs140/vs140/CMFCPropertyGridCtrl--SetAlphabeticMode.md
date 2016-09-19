---
title: "CMFCPropertyGridCtrl::SetAlphabeticMode"
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
ms.assetid: 9cd2f942-8872-4642-8b8b-5ba629d4cd25
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::SetAlphabeticMode
Sets or resets alphabetic mode.  
  
## Syntax  
  
```  
void SetAlphabeticMode(  
   BOOL bSet=TRUE   
);  
```  
  
#### Parameters  
 [in] `bSet`  
 `TRUE` to set alphabetic mode; `FALSE` reset alphabetic mode. The default value is `TRUE`.  
  
## Remarks  
 When the property grid control is in alphabetic mode, the control sorts all the properties it contains by their property name.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)