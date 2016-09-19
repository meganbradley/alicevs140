---
title: "CMFCToolBarButton::GetProtectedCommands"
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
ms.assetid: f333d679-1197-4e47-8499-38876fa873a6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::GetProtectedCommands
Retrieves the list of commands that the user cannot customize.  
  
## Syntax  
  
```  
static const CList<UINT,UINT>& GetProtectedCommands();  
```  
  
## Return Value  
 The list of protected commands.  
  
## Remarks  
 In customization mode, the framework disables toolbar button commands that are protected. The user cannot perform drag-and-drop and edit operations on disabled toolbar buttons.  
  
 Use the [CMFCToolBarButton::SetProtectedCommands](../vs140/CMFCToolBarButton--SetProtectedCommands.md) method to define the list of protected commands.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::SetProtectedCommands](../vs140/CMFCToolBarButton--SetProtectedCommands.md)