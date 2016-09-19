---
title: "CMFCToolBarEditBoxButton::GetContextMenuID"
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
ms.assetid: 408b4623-624e-41d7-b5ab-e8e5349632b1
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::GetContextMenuID
Retrieves the resource ID of the shortcut menu that is associated with the button.  
  
## Syntax  
  
```  
UINT GetContextMenuID();  
```  
  
## Return Value  
 The resource ID of the shortcut menu that is associated with the button or 0 if the button has no associated shortcut menu.  
  
## Remarks  
 The framework uses the resource ID to create the shortcut menu when the user right-clicks on the button.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarEditBoxButton::SetContextMenuID](../vs140/CMFCToolBarEditBoxButton--SetContextMenuID.md)