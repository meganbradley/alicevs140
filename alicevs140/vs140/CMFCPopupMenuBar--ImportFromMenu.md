---
title: "CMFCPopupMenuBar::ImportFromMenu"
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
ms.assetid: 85862d7a-a5ca-4240-974e-97f0d037c7e6
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenuBar::ImportFromMenu
Imports popup menu buttons from a specified menu.  
  
## Syntax  
  
```  
virtual BOOL ImportFromMenu(  
   HMENU hMenu,  
   BOOL bShowAllCommands = FALSE  
);  
```  
  
#### Parameters  
 [in] `hMenu`  
 The menu from which to import the popup menu buttons.  
  
 [in] `bShowAllCommands`  
 `TRUE` if all commands on the menu are to be imported, or `FALSE` if rarely used ones may be hidden.  
  
## Return Value  
 Returns `TRUE` if the menu buttons were successfully imported from the menu, or `FALSE` if not.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpopupmenubar.h  
  
## See Also  
 [CMFCPopupMenuBar Class](../vs140/CMFCPopupMenuBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)