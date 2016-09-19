---
title: "CMFCPopupMenu::EnableMenuSound"
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
ms.assetid: f77fe306-9ea2-4003-845c-526a21d88581
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::EnableMenuSound
Enables menu sound.  
  
## Syntax  
  
```  
static void EnableMenuSound(  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to enable sound, `FALSE` otherwise.  
  
## Remarks  
 If you enable sound, the framework calls the [PlaySound](http://msdn.microsoft.com/library/windows/desktop/bb774426) method when a user opens a pop-up menu or selects a menu command. By default, this feature is enabled.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)