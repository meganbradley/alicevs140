---
title: "CMFCToolBarEditBoxButton::SetContextMenuID"
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
ms.assetid: 92434b67-9181-4e70-a0d4-351213c74485
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::SetContextMenuID
Specifies the resource ID of the shortcut menu that is associated with the button.  
  
## Syntax  
  
```  
void SetContextMenuID(UINT uiResID);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The resource ID of the shortcut menu.  
  
## Remarks  
 The framework uses the resource ID to create the shortcut menu when the user right-clicks the toolbar button.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarEditBoxButton::GetContextMenuID](../vs140/CMFCToolBarEditBoxButton--GetContextMenuID.md)