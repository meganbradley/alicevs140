---
title: "CToolBarCtrl::CheckButton"
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
ms.assetid: 74d1a6c8-7400-4322-aa95-c2729df74083
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::CheckButton
Checks or clears a given button in a toolbar control.  
  
## Syntax  
  
```  
  
      BOOL CheckButton(  
   int nID,  
   BOOL bCheck = TRUE   
);  
```  
  
#### Parameters  
 `nID`  
 Command identifier of the button to check or clear.  
  
 *bCheck*  
 **TRUE** to check the button, **FALSE** to clear it.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 When a button has been checked, it appears to have been pressed. If you want to change more than one button state, consider calling [SetState](../vs140/CToolBarCtrl--SetState.md) instead.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::IsButtonChecked](../vs140/CToolBarCtrl--IsButtonChecked.md)   
 [CToolBarCtrl::EnableButton](../vs140/CToolBarCtrl--EnableButton.md)   
 [CToolBarCtrl::PressButton](../vs140/CToolBarCtrl--PressButton.md)   
 [CToolBarCtrl::HideButton](../vs140/CToolBarCtrl--HideButton.md)   
 [CToolBarCtrl::Indeterminate](../vs140/CToolBarCtrl--Indeterminate.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::SetState](../vs140/CToolBarCtrl--SetState.md)