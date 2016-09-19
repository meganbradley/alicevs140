---
title: "CDockablePane::OnPressButtons"
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
ms.assetid: 979f628a-4123-4f87-bfed-e3ac636a1c07
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::OnPressButtons
Called when the user presses a caption button other than the `AFX_HTCLOSE` and `AFX_HTMAXBUTTON` buttons.  
  
## Syntax  
  
```  
virtual void OnPressButtons(  
    UINT nHit  
);  
```  
  
#### Parameters  
 [in] `nHit`  
 This parameter is not used.  
  
## Remarks  
 If you add a custom button to the caption of a dockable pane, override this method to receive notifications when a user presses the button.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)