---
title: "CMFCToolBarButton::IsEditable"
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
ms.assetid: 826d1b21-634b-4e7b-9f83-27190685f1bc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::IsEditable
Determines whether the button can be customized.  
  
## Syntax  
  
```  
virtual BOOL IsEditable() const;  
```  
  
## Return Value  
 Nonzero if a button can be customized by the user; otherwise 0.  
  
## Remarks  
 The framework calls this method to determine whether the user can customize the toolbar button by using drag-and-drop or edit operations.  
  
 The default implementation returns `FALSE` if the command ID of the button is a standard command (you can determine this by calling the `IsStandardCommand` function) or if the command ID is in the list of protected commands. For more information about protected commands, see [CMFCToolBarButton::GetProtectedCommands](../vs140/CMFCToolBarButton--GetProtectedCommands.md) and [CMFCToolBarButton::SetProtectedCommands](../vs140/CMFCToolBarButton--SetProtectedCommands.md).  
  
 Override this method to customize its behavior.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::GetProtectedCommands](../vs140/CMFCToolBarButton--GetProtectedCommands.md)   
 [CMFCToolBarButton::SetProtectedCommands](../vs140/CMFCToolBarButton--SetProtectedCommands.md)