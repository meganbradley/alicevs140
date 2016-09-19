---
title: "CToolBarCtrl::SetState"
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
ms.assetid: 8497e6ec-7b8c-4077-a51c-2d7d86602a64
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetState
Sets the state for the specified button in a toolbar control.  
  
## Syntax  
  
```  
  
      BOOL SetState(  
   int nID,  
   UINT nState   
);  
```  
  
#### Parameters  
 `nID`  
 Command identifier of the button.  
  
 `nState`  
 State flags. It can be a combination of the values listed for button states in [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md).  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This function is especially handy if you want to set more than one of the button states. To just set one state, use one of the following member functions: [EnableButton](../vs140/CToolBarCtrl--EnableButton.md), [CheckButton](../vs140/CToolBarCtrl--CheckButton.md), [HideButton](../vs140/CToolBarCtrl--HideButton.md), [Indeterminate](../vs140/CToolBarCtrl--Indeterminate.md), or [PressButton](../vs140/CToolBarCtrl--PressButton.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md)   
 [CToolBarCtrl::EnableButton](../vs140/CToolBarCtrl--EnableButton.md)   
 [CToolBarCtrl::CheckButton](../vs140/CToolBarCtrl--CheckButton.md)   
 [CToolBarCtrl::HideButton](../vs140/CToolBarCtrl--HideButton.md)   
 [CToolBarCtrl::Indeterminate](../vs140/CToolBarCtrl--Indeterminate.md)   
 [CToolBarCtrl::PressButton](../vs140/CToolBarCtrl--PressButton.md)