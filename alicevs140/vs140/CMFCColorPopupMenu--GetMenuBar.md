---
title: "CMFCColorPopupMenu::GetMenuBar"
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
ms.assetid: d9f8239e-fb3a-4d17-8a34-797959b3fcb5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorPopupMenu::GetMenuBar
Returns the [CMFCPopupMenuBar](../vs140/CMFCPopupMenuBar-Class.md) that is embedded inside the pop-up menu.  
  
## Syntax  
  
```  
virtual CMFCPopupMenuBar* GetMenuBar();  
```  
  
## Return Value  
 A pointer to the embedded `CMFCPopupMenuBar`.  
  
## Remarks  
 The color pop-up menu has an embedded [CMFCPopupMenuBar Class](../vs140/CMFCPopupMenuBar-Class.md) object. Override this method in a derived class if your application uses a different embedded type.  
  
## Requirements  
 **Header:** afxcolorpopupmenu.h  
  
## See Also  
 [CMFCColorPopupMenu Class](../vs140/CMFCColorPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPopupMenuBar Class](../vs140/CMFCPopupMenuBar-Class.md)