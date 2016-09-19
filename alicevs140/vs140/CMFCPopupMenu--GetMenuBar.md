---
title: "CMFCPopupMenu::GetMenuBar"
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
ms.assetid: 583e6751-ebb0-48e1-ac25-376733a90b5c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::GetMenuBar
Returns the [CMFCPopupMenuBar](../vs140/CMFCPopupMenuBar-Class.md) embedded inside the pop-up menu.  
  
## Syntax  
  
```  
virtual CMFCPopupMenuBar* GetMenuBar();  
```  
  
## Return Value  
 A pointer to the embedded `CMFCPopupMenuBar`.  
  
## Remarks  
 The pop-up menu has an embedded `CMFCPopupMenuBar` object. You must override this method in a derived class if you are using a different embedded class.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPopupMenuBar Class](../vs140/CMFCPopupMenuBar-Class.md)