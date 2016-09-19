---
title: "CMFCPropertyGridCtrl::GetDescriptionHeight"
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
ms.assetid: 07627979-f853-4b64-afe9-85660d1fc46d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::GetDescriptionHeight
Retrieves the height of the description area, which is located at the bottom of the property grid control.  
  
## Syntax  
  
```  
int GetDescriptionHeight() const;  
```  
  
## Return Value  
 The height of the description area, in pixels.  
  
## Remarks  
 The height of the description area is calculated automatically and is set to 1/4 the height of the property grid control.  
  
 Use the [CMFCPropertyGridCtrl::EnableDescriptionArea](../vs140/CMFCPropertyGridCtrl--EnableDescriptionArea.md) method to display or hide the description area. Use the [CMFCPropertyGridCtrl::IsDescriptionArea](../vs140/CMFCPropertyGridCtrl--IsDescriptionArea.md) method to determine whether the description area is displayed or hidden.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)