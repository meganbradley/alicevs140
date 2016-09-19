---
title: "CMFCPropertyGridCtrl::UpdateColor"
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
ms.assetid: 957ede1d-b409-4b66-9044-718b4858b82d
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::UpdateColor
Sets the color value of the currently selected color property.  
  
## Syntax  
  
```  
virtual void UpdateColor(  
   COLORREF color  
);  
```  
  
#### Parameters  
 [in] `color`  
 An RGB color value.  
  
## Remarks  
 This method asserts in debug mode if the currently selected property of the property grid control is not a color property.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridColorProperty Class](../vs140/CMFCPropertyGridColorProperty-Class.md)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)