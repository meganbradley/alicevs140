---
title: "CMFCToolBarButton::OnCustomizeMenu"
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
ms.assetid: 30425651-7c31-49c5-8d08-30e4fcfb1322
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::OnCustomizeMenu
Allows the button to modify the provided menu when the application displays a shortcut menu on the parent toolbar.  
  
## Syntax  
  
```  
virtual BOOL OnCustomizeMenu(  
   CMenu* pMenu  
);  
```  
  
#### Parameters  
 [in] `pMenu`  
 The menu to customize.  
  
## Return Value  
 This method returns `FALSE`.  
  
## Remarks  
 The default implementation does nothing and returns `FALSE`. Override this method and return a nonzero value if you want to modify the contents of the provided menu.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)