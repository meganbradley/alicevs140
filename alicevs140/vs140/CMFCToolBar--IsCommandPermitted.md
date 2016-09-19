---
title: "CMFCToolBar::IsCommandPermitted"
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
ms.assetid: a475875e-b778-4d0c-a179-ee8da552f1be
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::IsCommandPermitted
Determines whether a command is permitted.  
  
## Syntax  
  
```  
static BOOL IsCommandPermitted(  
   UINT uiCmd   
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 Specifies the command to check.  
  
## Return Value  
 `TRUE` if the specified command is permitted; otherwise `FALSE`.  
  
## Remarks  
 This static method determines whether the command specified by `uiCmd` belongs to the global list of non-permitted commands.  
  
 You can change the list of non-permitted commands by calling [CMFCToolBar::SetNonPermittedCommands](../vs140/CMFCToolBar--SetNonPermittedCommands.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)