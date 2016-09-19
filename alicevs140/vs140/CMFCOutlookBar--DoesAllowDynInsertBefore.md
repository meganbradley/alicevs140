---
title: "CMFCOutlookBar::DoesAllowDynInsertBefore"
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
ms.assetid: e3c05cfc-4c74-4d71-aaa1-5482425531d8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBar::DoesAllowDynInsertBefore
Specifies whether a user can dock a pane at the outer edge of the Outlook bar.  
  
## Syntax  
  
```  
DECLARE_MESSAGE_MAP virtual BOOL DoesAllowDynInsertBefore() const;  
```  
  
## Return Value  
 The default implementation returns `FALSE`.  
  
## Remarks  
 The framework calls the `DoesAllowDynInsertBefore` method when it looks for a location to dock a dynamic pane. If the function returns `FALSE`, the framework does not allow the docking of any dynamic pane at the outer edges of the pane.  
  
 Usually, you create an Outlook bar as a static non-floating control. You can override this function in a derived class and return `TRUE` to change this behavior.  
  
> [!NOTE]
>  Because dynamic panes check the status of docked static panes when docking, you should dock dynamic panes after static panes whenever possible.  
  
## Requirements  
 **Header:** afxoutlookbar.h  
  
## See Also  
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)