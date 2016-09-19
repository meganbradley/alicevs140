---
title: "COleControlSite::SetFocus"
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
ms.assetid: fdbef03c-d449-41a0-a8b1-99aaf06508a8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::SetFocus
Sets focus to the control.  
  
## Syntax  
  
```  
  
      virtual CWnd* SetFocus( );   
virtual CWnd* SetFocus(   
   LPMSG lpmsg   
);  
```  
  
#### Parameters  
 *lpmsg*  
 A pointer to a [MSG](../vs140/MSG-Structure.md) structure. This structure contains the Windows message triggering the `SetFocus` request for the control contained in the current control site.  
  
## Return Value  
 A pointer to the window that previously had focus.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)