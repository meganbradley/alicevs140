---
title: "CToolBarCtrl::IsButtonIndeterminate"
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
ms.assetid: 5e51d32b-3278-4c2d-b107-655555359ca6
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::IsButtonIndeterminate
Determines whether the specified button in a toolbar control is indeterminate.  
  
## Syntax  
  
```  
BOOL IsButtonIndeterminate(  
   int nID   
) const;  
```  
  
#### Parameters  
 [in] `nID`  
 Command identifier of the button in the toolbar.  
  
## Return Value  
 Positive integer if the button is indeterminate, zero if the button is not indeterminate, or -1 if an error occurs.  
  
## Remarks  
 Indeterminate buttons are displayed dimmed, such as the way the bold button on the toolbar of a word processor looks when the selected text contains both bold and regular characters. Consider calling [GetState](../vs140/CToolBarCtrl--GetState.md) if you want to retrieve more than one button state.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::Indeterminate](../vs140/CToolBarCtrl--Indeterminate.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::SetState](../vs140/CToolBarCtrl--SetState.md)   
 [CToolBarCtrl::IsButtonEnabled](../vs140/CToolBarCtrl--IsButtonEnabled.md)   
 [CToolBarCtrl::IsButtonChecked](../vs140/CToolBarCtrl--IsButtonChecked.md)   
 [CToolBarCtrl::IsButtonPressed](../vs140/CToolBarCtrl--IsButtonPressed.md)   
 [CToolBarCtrl::IsButtonHidden](../vs140/CToolBarCtrl--IsButtonHidden.md)   
 [CToolBarCtrl::IsButtonHighlighted](../vs140/CToolBarCtrl--IsButtonHighlighted.md)