---
title: "CToolTipCtrl::Activate"
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
ms.assetid: 138d65e0-0d7c-4498-a5bc-67675b947f60
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::Activate
Call this function to activate or deactivate a tool tip control.  
  
## Syntax  
  
```  
  
      void Activate(   
   BOOL bActivate    
);  
```  
  
#### Parameters  
 `bActivate`  
 Specifies whether the tool tip control is to be activated or deactivated.  
  
## Remarks  
 If `bActivate` is **TRUE**, the control is activated; if **FALSE**, it is deactivated.  
  
 When a tool tip control is active, the tool tip information appears when the cursor is on a tool that is registered with the control; when it is inactive, the tool tip information does not appear, even when the cursor is on a tool.  
  
## Example  
 See the example for [CPropertySheet::GetTabControl](../vs140/CPropertySheet--GetTabControl.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::UpdateTipText](../vs140/CToolTipCtrl--UpdateTipText.md)   
 [CToolTipCtrl::SetDelayTime](../vs140/CToolTipCtrl--SetDelayTime.md)