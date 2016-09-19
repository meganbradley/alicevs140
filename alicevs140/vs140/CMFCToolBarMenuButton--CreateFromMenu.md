---
title: "CMFCToolBarMenuButton::CreateFromMenu"
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
ms.assetid: d651d0b7-914a-41ca-812c-002abd88643c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::CreateFromMenu
Initializes the toolbar menu from a Windows menu handle.  
  
## Syntax  
  
```  
virtual void CreateFromMenu(  
   HMENU hMenu   
);  
```  
  
#### Parameters  
 [in] `hMenu`  
 A handle to a menu.  
  
## Remarks  
 A toolbar menu button can display a drop-down submenu.  
  
 The framework calls this method to initialize the commands in the submenu from a menu.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)