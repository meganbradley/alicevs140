---
title: "CMFCToolTipCtrl::OnDrawIcon"
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
ms.assetid: 534a290d-6dac-4f1f-a866-599b5d1234fb
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolTipCtrl::OnDrawIcon
Displays an icon in a tooltip.  
  
## Syntax  
  
```  
virtual BOOL OnDrawIcon(  
   CDC* pDC,  
   CRect rectImage   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectImage`  
 Coordinates of the icon.  
  
## Return Value  
 `TRUE` if the icon was drawn. Otherwise `FALSE`.  
  
## Remarks  
 Override this method in a derived class to display a custom icon. You must also override [CMFCToolTipCtrl::GetIconSize](../vs140/CMFCToolTipCtrl--GetIconSize.md) to enable the tooltip to correctly calculate the layout of text and description.  
  
## Requirements  
 **Header:** afxToolTipCtrl.h  
  
## See Also  
 [CMFCToolTipCtrl Class](../vs140/CMFCToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)