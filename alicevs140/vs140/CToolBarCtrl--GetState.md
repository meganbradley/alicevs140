---
title: "CToolBarCtrl::GetState"
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
ms.assetid: 39b93533-b17e-4385-b5d9-eedd4f0efb93
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetState
Retrieves information about the state of the specified button in a toolbar control, such as whether it is enabled, pressed, or checked.  
  
## Syntax  
  
```  
  
      int GetState(  
   int nID   
) const;  
```  
  
#### Parameters  
 `nID`  
 Command identifier of the button for which to retrieve information.  
  
## Return Value  
 The button state information if successful or – 1 otherwise. The button state information can be a combination of the values listed in [CToolBarCtrl::AddButtons](../vs140/CToolBarCtrl--AddButtons.md).  
  
## Remarks  
 This function is especially handy if you want to retrieve more than one of the button states. To just retrieve one state, use one of the following member functions: [IsButtonEnabled](../vs140/CToolBarCtrl--IsButtonEnabled.md), [IsButtonChecked](../vs140/CToolBarCtrl--IsButtonChecked.md), [IsButtonPressed](../vs140/CToolBarCtrl--IsButtonPressed.md), [IsButtonHidden](../vs140/CToolBarCtrl--IsButtonHidden.md), or [IsButtonIndeterminate](../vs140/CToolBarCtrl--IsButtonIndeterminate.md). However, the `GetState` member function is the only way to detect the `TBSTATE_WRAP` button state.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetState](../vs140/CToolBarCtrl--SetState.md)   
 [CToolBarCtrl::GetItemRect](../vs140/CToolBarCtrl--GetItemRect.md)   
 [CToolBarCtrl::IsButtonEnabled](../vs140/CToolBarCtrl--IsButtonEnabled.md)   
 [CToolBarCtrl::IsButtonChecked](../vs140/CToolBarCtrl--IsButtonChecked.md)   
 [CToolBarCtrl::IsButtonPressed](../vs140/CToolBarCtrl--IsButtonPressed.md)   
 [CToolBarCtrl::IsButtonHidden](../vs140/CToolBarCtrl--IsButtonHidden.md)   
 [CToolBarCtrl::IsButtonIndeterminate](../vs140/CToolBarCtrl--IsButtonIndeterminate.md)