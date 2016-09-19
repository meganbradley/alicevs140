---
title: "CPane::AllowShowOnPaneMenu"
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
ms.assetid: 05869842-3b05-4640-9957-18603c25476b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::AllowShowOnPaneMenu
Specifies whether the pane is listed in the runtime-generated list of panes for the application.  
  
## Syntax  
  
```  
virtual BOOL AllowShowOnPaneMenu() const;  
```  
  
## Return Value  
 `TRUE` if the pane is displayed in the list; otherwise, `FALSE`. The base implementation always returns `TRUE`.  
  
## Remarks  
 The AppWizard-generated application contains a menu option that lists panes that it contains. This method determines whether the pane is displayed in the list.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)