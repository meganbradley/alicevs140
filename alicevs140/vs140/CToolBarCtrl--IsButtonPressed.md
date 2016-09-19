---
title: "CToolBarCtrl::IsButtonPressed"
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
ms.assetid: 455b7e24-eb87-4cb3-be45-016e50bee4ad
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::IsButtonPressed
Determines whether the specified button in a toolbar control is pressed.  
  
## Syntax  
  
```  
  
      BOOL IsButtonPressed(  
   int nID   
) const;  
```  
  
#### Parameters  
 `nID`  
 Command identifier of the button in the toolbar.  
  
## Return Value  
 Nonzero if the button is pressed, otherwise zero.  
  
## Remarks  
 Consider calling [GetState](../vs140/CToolBarCtrl--GetState.md) if you want to retrieve more than one button state.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::PressButton](../vs140/CToolBarCtrl--PressButton.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::SetState](../vs140/CToolBarCtrl--SetState.md)   
 [CToolBarCtrl::IsButtonEnabled](../vs140/CToolBarCtrl--IsButtonEnabled.md)   
 [CToolBarCtrl::IsButtonChecked](../vs140/CToolBarCtrl--IsButtonChecked.md)   
 [CToolBarCtrl::IsButtonHidden](../vs140/CToolBarCtrl--IsButtonHidden.md)   
 [CToolBarCtrl::IsButtonIndeterminate](../vs140/CToolBarCtrl--IsButtonIndeterminate.md)   
 [CToolBarCtrl::IsButtonHighlighted](../vs140/CToolBarCtrl--IsButtonHighlighted.md)