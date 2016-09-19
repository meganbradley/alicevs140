---
title: "CToolBarCtrl::IsButtonChecked"
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
ms.assetid: dc5f2ea1-4bae-466e-aee1-968796670d3f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::IsButtonChecked
Determines whether the specified button in a toolbar control is checked.  
  
## Syntax  
  
```  
  
      BOOL IsButtonChecked(  
   int nID   
) const;  
```  
  
#### Parameters  
 `nID`  
 Command identifier of the button in the toolbar.  
  
## Return Value  
 Nonzero if the button is checked; otherwise zero.  
  
## Remarks  
 Consider calling [GetState](../vs140/CToolBarCtrl--GetState.md) if you want to retrieve more than one button state.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::CheckButton](../vs140/CToolBarCtrl--CheckButton.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::SetState](../vs140/CToolBarCtrl--SetState.md)   
 [CToolBarCtrl::IsButtonEnabled](../vs140/CToolBarCtrl--IsButtonEnabled.md)   
 [CToolBarCtrl::IsButtonPressed](../vs140/CToolBarCtrl--IsButtonPressed.md)   
 [CToolBarCtrl::IsButtonHidden](../vs140/CToolBarCtrl--IsButtonHidden.md)   
 [CToolBarCtrl::IsButtonIndeterminate](../vs140/CToolBarCtrl--IsButtonIndeterminate.md)   
 [CToolBarCtrl::IsButtonHighlighted](../vs140/CToolBarCtrl--IsButtonHighlighted.md)