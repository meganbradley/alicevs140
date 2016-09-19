---
title: "CMFCToolBar::InsertSeparator"
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
ms.assetid: 3136f9f2-53e8-416f-8f08-225383a8678c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::InsertSeparator
Inserts a separator into the toolbar.  
  
## Syntax  
  
```  
virtual int InsertSeparator(  
   INT_PTR iInsertAt=-1   
);  
```  
  
#### Parameters  
 [in] `iInsertAt`  
 Specifies the zero-based position to insert the separator at. This parameter must be larger than 0.  
  
## Return Value  
 The position at which the separator was inserted or -1 if an error occurs.  
  
## Remarks  
 Call this method to insert a separator between two existing buttons. If `iInsertAt` is -1, this method adds the separator to the end of the list of toolbar buttons.  
  
 You cannot use this method to add a separator to an empty toolbar.  
  
 Call the [CMFCToolBar::InsertButton](../vs140/CMFCToolBar--InsertButton.md) method to insert a button into the toolbar.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::InsertButton](../vs140/CMFCToolBar--InsertButton.md)