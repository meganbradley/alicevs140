---
title: "CMFCToolBar::SetNonPermittedCommands"
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
ms.assetid: 3e95179f-a7ca-4c09-aa87-b47d44e15ad1
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetNonPermittedCommands
Sets the list of commands that cannot be executed by the user.  
  
## Syntax  
  
```  
static void SetNonPermittedCommands(  
   CList<UINT,UINT>& lstCommands   
);  
```  
  
#### Parameters  
 [in] `lstCommands`  
 A reference to a `CList` object that contains the commands that cannot be executed by the user.  
  
## Remarks  
 Call this method to prevent the user from selecting certain commands. For example, you might want to prevent the user from selecting certain commands for security reasons. See the MDITabsDemo and MenuSubSet samples for examples that use this method.  
  
 This method clears the previous list of non-permitted commands. By default, the list of non-permitted commands is empty.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)