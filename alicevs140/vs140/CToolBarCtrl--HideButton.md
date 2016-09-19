---
title: "CToolBarCtrl::HideButton"
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
ms.assetid: 0fcac56f-4437-49df-972d-23325b153edc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::HideButton
Hides or shows the specified button in a toolbar control.  
  
## Syntax  
  
```  
  
      BOOL HideButton(  
   int nID,  
   BOOL bHide = TRUE   
);  
```  
  
#### Parameters  
 `nID`  
 Command identifier of the button to hide or show.  
  
 `bHide`  
 **TRUE** to hide the button, **FALSE** to show it.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 If you want to change more than one button state, consider calling [SetState](../vs140/CToolBarCtrl--SetState.md) instead.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::IsButtonHidden](../vs140/CToolBarCtrl--IsButtonHidden.md)   
 [CToolBarCtrl::EnableButton](../vs140/CToolBarCtrl--EnableButton.md)   
 [CToolBarCtrl::CheckButton](../vs140/CToolBarCtrl--CheckButton.md)   
 [CToolBarCtrl::PressButton](../vs140/CToolBarCtrl--PressButton.md)   
 [CToolBarCtrl::Indeterminate](../vs140/CToolBarCtrl--Indeterminate.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::SetState](../vs140/CToolBarCtrl--SetState.md)