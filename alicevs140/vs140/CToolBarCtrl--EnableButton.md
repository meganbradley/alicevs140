---
title: "CToolBarCtrl::EnableButton"
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
ms.assetid: dc8ece3d-5794-4c76-adc0-e551d369d063
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::EnableButton
Enables or disables the specified button in a toolbar control.  
  
## Syntax  
  
```  
  
      BOOL EnableButton(  
   int nID,  
   BOOL bEnable = TRUE   
);  
```  
  
#### Parameters  
 `nID`  
 Command identifier of the button to enable or disable.  
  
 `bEnable`  
 **TRUE** to enable the button; **FALSE** to disable the button.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 When a button has been enabled, it can be pressed and checked. If you want to change more than one button state, consider calling [SetState](../vs140/CToolBarCtrl--SetState.md) instead.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::IsButtonEnabled](../vs140/CToolBarCtrl--IsButtonEnabled.md)   
 [CToolBarCtrl::CheckButton](../vs140/CToolBarCtrl--CheckButton.md)   
 [CToolBarCtrl::PressButton](../vs140/CToolBarCtrl--PressButton.md)   
 [CToolBarCtrl::HideButton](../vs140/CToolBarCtrl--HideButton.md)   
 [CToolBarCtrl::Indeterminate](../vs140/CToolBarCtrl--Indeterminate.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::SetState](../vs140/CToolBarCtrl--SetState.md)