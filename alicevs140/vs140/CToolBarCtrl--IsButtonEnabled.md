---
title: "CToolBarCtrl::IsButtonEnabled"
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
ms.assetid: ea16aba1-ffd1-4683-817e-f60270c698d8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::IsButtonEnabled
Determines whether the specified button in a toolbar control is enabled.  
  
## Syntax  
  
```  
  
      BOOL IsButtonEnabled(  
   int nID   
) const;  
```  
  
#### Parameters  
 `nID`  
 Command identifier of the button in the toolbar.  
  
## Return Value  
 Nonzero if the button is enabled; otherwise zero.  
  
## Remarks  
 Consider calling [GetState](../vs140/CToolBarCtrl--GetState.md) if you want to retrieve more than one button state.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::EnableButton](../vs140/CToolBarCtrl--EnableButton.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::SetState](../vs140/CToolBarCtrl--SetState.md)   
 [CToolBarCtrl::IsButtonChecked](../vs140/CToolBarCtrl--IsButtonChecked.md)   
 [CToolBarCtrl::IsButtonPressed](../vs140/CToolBarCtrl--IsButtonPressed.md)   
 [CToolBarCtrl::IsButtonHidden](../vs140/CToolBarCtrl--IsButtonHidden.md)   
 [CToolBarCtrl::IsButtonIndeterminate](../vs140/CToolBarCtrl--IsButtonIndeterminate.md)   
 [CToolBarCtrl::IsButtonHighlighted](../vs140/CToolBarCtrl--IsButtonHighlighted.md)