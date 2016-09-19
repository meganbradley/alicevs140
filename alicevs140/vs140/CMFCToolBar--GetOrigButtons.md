---
title: "CMFCToolBar::GetOrigButtons"
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
ms.assetid: 76ccb57c-de94-4b2f-8079-b02faf9057ff
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetOrigButtons
Retrieves the collection of non-customized buttons of the toolbar.  
  
## Syntax  
  
```  
const CObList& GetOrigButtons() const;  
```  
  
## Return Value  
 A reference to the list of non-customized buttons of the toolbar.  
  
## Remarks  
 The framework creates a copy of toolbar buttons before they are customized by the user. The [CMFCToolBar::SetButtons](../vs140/CMFCToolBar--SetButtons.md) method adds a copy of each button in the provided array to the list of original buttons. The [CMFCToolBar::RestoreOriginalstate](../vs140/CMFCToolBar--RestoreOriginalState.md) method restores the original state of the toolbar by loading it from the resource file.  
  
 To set the list of original buttons for your toolbar, call the [CMFCToolBar::SetOrigButtons](../vs140/CMFCToolBar--SetOrigButtons.md) method.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::SetButtons](../vs140/CMFCToolBar--SetButtons.md)   
 [CMFCToolBar::RestoreOriginalstate](../vs140/CMFCToolBar--RestoreOriginalState.md)   
 [CMFCToolBar::SetOrigButtons](../vs140/CMFCToolBar--SetOrigButtons.md)