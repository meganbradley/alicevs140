---
title: "CMFCBaseTabCtrl::SetTabLabel"
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
ms.assetid: c8f86e89-b3d4-421e-ab1a-15bd8aaa7df3
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::SetTabLabel
Sets the text for a tab label.  
  
## Syntax  
  
```  
virtual BOOL SetTabLabel(  
   int iTab,  
   const CString& strLabel  
);  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of the tab to update.  
  
 [in] `strLabel`  
 A reference to a string that contains the new text for the tab label.  
  
## Return Value  
 Nonzero if successful; 0 otherwise.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)