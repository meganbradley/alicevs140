---
title: "CMFCToolBarButton::SetProtectedCommands"
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
ms.assetid: 2d8cfdf6-262d-45eb-9c6c-8f1b31116e57
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::SetProtectedCommands
Sets the list of commands that the user cannot customize.  
  
## Syntax  
  
```  
static void SetProtectedCommands(  
   const CList<UINT,UINT>& lstCmds   
);  
```  
  
#### Parameters  
 [in] `lstCmds`  
 The list of protected commands.  
  
## Remarks  
 In customization mode, the framework disables toolbar button commands that are protected. The user cannot perform drag-and-drop and edit operations on disabled toolbar buttons.  
  
 Use the [CMFCToolBarButton::GetProtectedCommands](../vs140/CMFCToolBarButton--GetProtectedCommands.md) method to retrieve the list of protected commands.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::GetProtectedCommands](../vs140/CMFCToolBarButton--GetProtectedCommands.md)