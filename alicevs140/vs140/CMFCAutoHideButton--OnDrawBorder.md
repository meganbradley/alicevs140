---
title: "CMFCAutoHideButton::OnDrawBorder"
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
ms.assetid: a5378dfb-bf0b-49e9-9dc6-2e95326bf565
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAutoHideButton::OnDrawBorder
The framework calls this method when it draws the border of an auto-hide button.  
  
## Syntax  
  
```  
virtual void OnDrawBorder(  
   CDC* pDC,  
   CRect rectBounds,  
   CRect rectBorderSize   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectBounds`  
 The bounding rectangle of the auto-hide button.  
  
 [in] `rectBorderSize`  
 The border thickness for each side of the auto-hide button.  
  
## Remarks  
 If you want to customize the border of each auto-hide button in your application, create a new class derived from the [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md). In your derived class, override this method.  
  
## Requirements  
 **Header:** afxautohidebutton.h  
  
## See Also  
 [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)