---
title: "CMFCDropDownToolbarButton::SetDefaultCommand"
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
ms.assetid: 4603148f-9942-4c13-8517-55cee745c101
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::SetDefaultCommand
Sets the default command that the framework uses when a user clicks the button.  
  
## Syntax  
  
```  
void SetDefaultCommand(  
   UINT uiCmd  
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The ID of the default command.  
  
## Remarks  
 Call this method to specify a default command that the framework executes when the user clicks the button. An item with the command ID specified by `uiCmd` must be located in the parent drop-down toolbar.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)