---
title: "CMFCPropertySheet::InitNavigationControl"
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
ms.assetid: 8d809091-02aa-4b73-ac12-a29e727edde8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertySheet::InitNavigationControl
Initializes the appearance of the current property sheet control.  
  
## Syntax  
  
```  
virtual CWnd* InitNavigationControl();  
```  
  
## Return Value  
 A pointer to the window of the property sheet control.  
  
## Remarks  
 A property sheet control can appear in several different forms, such as a set of tabbed pages, a tree control, or a list of navigation buttons. Use the [CMFCPropertySheet::SetLook](../vs140/CMFCPropertySheet--SetLook.md) method to specify the appearance of the property sheet control.  
  
## Requirements  
 **Header:** afxpropertysheet.h  
  
## See Also  
 [CMFCPropertySheet Class](../vs140/CMFCPropertySheet-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertySheet::SetLook](../vs140/CMFCPropertySheet--SetLook.md)