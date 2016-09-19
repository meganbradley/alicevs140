---
title: "CSpinButtonCtrl::SetBuddy"
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
ms.assetid: 1b6d3583-0a3e-4296-991a-4f95904ec24e
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSpinButtonCtrl::SetBuddy
Sets the buddy window for a spin button control.  
  
## Syntax  
  
```  
  
      CWnd* SetBuddy(  
   CWnd* pWndBuddy   
);  
```  
  
#### Parameters  
 `pWndBuddy`  
 Pointer to the new buddy window.  
  
## Return Value  
 A pointer to the previous buddy window.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Remarks  
 A spin control is almost always associated with another window, such as an edit control, that displays some content. This other window is called the "buddy" of the spin control.  
  
## See Also  
 [CSpinButtonCtrl Class](../vs140/CSpinButtonCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSpinButtonCtrl::GetBuddy](../vs140/CSpinButtonCtrl--GetBuddy.md)