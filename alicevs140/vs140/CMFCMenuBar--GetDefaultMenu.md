---
title: "CMFCMenuBar::GetDefaultMenu"
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
ms.assetid: d7fd7943-30df-4680-958d-95f32774ad67
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::GetDefaultMenu
Retrieves a handle to the original menu. The framework loads the original menu from the resource file.  
  
## Syntax  
  
```  
HMENU GetDefaultMenu() const;  
```  
  
## Return Value  
 A handle to a menu resource.  
  
## Remarks  
 If your application customizes a menu, you can use this method to retrieve a handle to the original menu.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)