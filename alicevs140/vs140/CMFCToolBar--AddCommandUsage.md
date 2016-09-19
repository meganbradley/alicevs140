---
title: "CMFCToolBar::AddCommandUsage"
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
ms.assetid: 7460e422-3008-49b6-8d12-1061c453b184
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::AddCommandUsage
Increments by one the counter that is associated with the given command.  
  
## Syntax  
  
```  
static void __stdcall AddCommandUsage(  
   UINT uiCommand  
);  
```  
  
#### Parameters  
 [in] `uiCommand`  
 Specifies the command counter to increment.  
  
## Remarks  
 The framework calls this method when the user selects a menu item.  
  
 The framework uses command counters to display recently used menu items.  
  
 This method increments the command counter by using the [CMFCCmdUsageCount::AddCmd](../vs140/CMFCCmdUsageCount--AddCmd.md) method.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCCmdUsageCount::AddCmd](../vs140/CMFCCmdUsageCount--AddCmd.md)