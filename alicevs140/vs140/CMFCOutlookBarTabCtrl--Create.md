---
title: "CMFCOutlookBarTabCtrl::Create"
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
ms.assetid: 4811d9a1-8b07-4151-a6a9-eaccc69a908c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarTabCtrl::Create
Creates the Outlook bar tab control.  
  
## Syntax  
  
```  
virtual BOOL Create(  
   const CRect& rect,  
   CWnd* pParentWnd,  
   UINT nID   
);  
```  
  
#### Parameters  
 [in] `rect`  
 Specifies the initial size and position, in pixels.  
  
 [in] `pParentWnd`  
 Points to the parent window. Must not be `NULL`.  
  
 [in] `nID`  
 The control ID.  
  
## Return Value  
 Nonzero if the control has been created successfully; otherwise 0.  
  
## Remarks  
 Usually, outlook bar tab controls are created when [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md) controls the  `WM_CREATE` message of the process.  
  
## Requirements  
 **Header:** afxOutlookBarTabCtrl.h  
  
## See Also  
 [CMFCOutlookBarTabCtrl Class](../vs140/CMFCOutlookBarTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)