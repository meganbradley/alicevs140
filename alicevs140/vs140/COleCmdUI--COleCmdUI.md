---
title: "COleCmdUI::COleCmdUI"
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
ms.assetid: 8776462c-72c8-4dfa-ac41-eba13544af13
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCmdUI::COleCmdUI
Constructs a `COleCmdUI` object associated with a particular user-interface command.  
  
## Syntax  
  
```  
  
      COleCmdUI(   
   OLECMD* rgCmds,   
   ULONG cCmds,   
   const GUID* m_pGroup    
);  
```  
  
#### Parameters  
 `rgCmds`  
 A list of supported commands associated with the given GUID. The **OLECMD** structure associates commands with command flags.  
  
 *cCmds*  
 The count of commands in `rgCmds`.  
  
 `pGroup`  
 A pointer to a GUID that identifies a set of commands.  
  
## Remarks  
 The `COleCmdUI` object provides a programmatic interface for updating DocObject user-interface objects such as menu items or control-bar buttons. The user-interface objects can be enabled, disabled, checked, and/or cleared through the `COleCmdUI` object.  
  
## Requirements  
 **Header:** afxdocob.h  
  
## See Also  
 [COleCmdUI Class](../vs140/COleCmdUI-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)