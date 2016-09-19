---
title: "CTabCtrl::SetCurFocus"
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
ms.assetid: 14a2b63e-b344-4c83-8ce6-79a2766035a1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::SetCurFocus
Sets the focus to a specified tab in a tab control.  
  
## Syntax  
  
```  
  
      void SetCurFocus(  
  int nItem   
);  
```  
  
#### Parameters  
 `nItem`  
 Specifies the index of the tab that gets the focus.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TCM_SETCURFOCUS](http://msdn.microsoft.com/library/windows/desktop/bb760610), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::SetCurSel](../vs140/CTabCtrl--SetCurSel.md)