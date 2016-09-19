---
title: "CToolBarCtrl::PressButton"
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
ms.assetid: 19d4f70d-b49a-43e2-8640-6c417f7f85da
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::PressButton
Presses or releases the specified button in a toolbar control.  
  
## Syntax  
  
```  
  
      BOOL PressButton(  
   int nID,  
   BOOL bPress = TRUE   
);  
```  
  
#### Parameters  
 [in] `nID`  
 Command identifier of the button to press or release.  
  
 [in] `bPress`  
 `true` to press the specified button; `false` to release the specified button. The default value is `true`.  
  
## Return Value  
 `true` if the method is successful; otherwise, `false`.  
  
## Remarks  
 If you want to change more than one button state, consider calling [SetState](../vs140/CToolBarCtrl--SetState.md) instead.  
  
 This method sends the [TB_PRESSBUTTON](http://msdn.microsoft.com/library/windows/desktop/bb787389) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::IsButtonPressed](../vs140/CToolBarCtrl--IsButtonPressed.md)   
 [CToolBarCtrl::EnableButton](../vs140/CToolBarCtrl--EnableButton.md)   
 [CToolBarCtrl::CheckButton](../vs140/CToolBarCtrl--CheckButton.md)   
 [CToolBarCtrl::HideButton](../vs140/CToolBarCtrl--HideButton.md)   
 [CToolBarCtrl::Indeterminate](../vs140/CToolBarCtrl--Indeterminate.md)   
 [CToolBarCtrl::GetState](../vs140/CToolBarCtrl--GetState.md)   
 [CToolBarCtrl::SetState](../vs140/CToolBarCtrl--SetState.md)