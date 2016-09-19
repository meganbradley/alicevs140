---
title: "CMFCCmdUsageCount::AddCmd"
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
ms.assetid: 791acba8-cc07-4f4b-bd55-2d3c6e1a733f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCmdUsageCount::AddCmd
Increments by one the counter that is associated with the given command.  
  
## Syntax  
  
```  
void AddCmd(  
   UINT uiCmd  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `uiCmd`|Specifies the command counter to increment.|  
  
## Remarks  
 This method adds a new entry to the map structure of command counts, `m_CmdUsage`, if the entry does not already exist.  
  
 This method does nothing in the following cases:  
  
-   The toolbar framework is in customization mode (the [CMFCToolBar::IsCustomizeMode](../vs140/CMFCToolBar--IsCustomizeMode.md) method returns a nonzero value).  
  
-   The command refers to a submenu or menu separator (`uiCmd` equals 0 or -1).  
  
-   `uiCmd` refers to a standard command (the global `IsStandardCommand` function returns a nonzero value).  
  
## Requirements  
 **Header:** afxcmdusagecount.h  
  
## See Also  
 [CMFCCmdUsageCount Class](../vs140/CMFCCmdUsageCount-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::IsCustomizeMode](../vs140/CMFCToolBar--IsCustomizeMode.md)