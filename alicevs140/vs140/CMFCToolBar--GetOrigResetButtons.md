---
title: "CMFCToolBar::GetOrigResetButtons"
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
ms.assetid: fa4eff78-3ac1-4fba-96e4-32c55cd255b8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetOrigResetButtons
Retrieves the collection of non-customized reset buttons of the toolbar.  
  
## Syntax  
  
```  
const CObList& GetOrigResetButtons() const;  
```  
  
## Return Value  
 A reference to the list of non-customized reset buttons of the toolbar.  
  
## Remarks  
 When the user clicks the **Reset** button during customization mode, the framework uses this method to restore buttons that were removed from the toolbar.  
  
 The [CMFCToolBar::SetButtons](../vs140/CMFCToolBar--SetButtons.md) method adds a copy of each toolbar button to the list of original reset buttons after it calls the [CMFCToolBar::OnReset](../vs140/CMFCToolBar--OnReset.md) method. You can override the [CMFCToolBar::OnReset](../vs140/CMFCToolBar--OnReset.md) method to customize the appearance of buttons after the user presses the **Reset** button.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::SetButtons](../vs140/CMFCToolBar--SetButtons.md)   
 [CMFCToolBar::OnReset](../vs140/CMFCToolBar--OnReset.md)