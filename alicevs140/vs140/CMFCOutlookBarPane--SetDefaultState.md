---
title: "CMFCOutlookBarPane::SetDefaultState"
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
ms.assetid: 67655aea-dd99-4cb9-a332-3254118dda52
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarPane::SetDefaultState
Resets the Outlook bar pane to the original set of buttons.  
  
## Syntax  
  
```  
void SetDefaultState();  
```  
  
## Remarks  
 This method restores the Outlook bar buttons to the original set. This method is like `CMFCOutlookBarPane::RestoreOriginalstate`, except that it does not trigger a redraw of the Outlook bar pane.  
  
## Requirements  
 **Header:** afxoutlookbarpane.h  
  
## See Also  
 [CMFCOutlookBarPane Class](../vs140/CMFCOutlookBarPane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)