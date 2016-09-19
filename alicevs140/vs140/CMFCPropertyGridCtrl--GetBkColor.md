---
title: "CMFCPropertyGridCtrl::GetBkColor"
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
ms.assetid: a7c7637a-be88-4889-afeb-6bffca3027a8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::GetBkColor
Retrieves the background color of the current property grid control.  
  
## Syntax  
  
```  
COLORREF GetBkColor() const;  
```  
  
## Return Value  
 An RGB color value.  
  
## Remarks  
 This method retrieves the color that the framework uses to draw the background of the current property grid control. The [CMFCPropertyGridCtrl::GetTextColor](../vs140/CMFCPropertyGridCtrl--GetTextColor.md) method retrieves the foreground color.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)   
 [CMFCPropertyGridCtrl::GetTextColor](../vs140/CMFCPropertyGridCtrl--GetTextColor.md)