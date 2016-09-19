---
title: "CFrameWndEx::OnToolbarCreateNew"
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
ms.assetid: 507f34b1-b3ce-4483-a04d-3c070128978f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnToolbarCreateNew
The framework calls this method to create a new toolbar.  
  
## Syntax  
  
```  
afx_msg LRESULT OnToolbarCreateNew(  
   WPARAM wp,  
   LPARAM lp  
);  
```  
  
#### Parameters  
 [in] `wp`  
 This parameter is not used.  
  
 [in] `lp`  
 Pointer to the text for the title bar of the toolbar.  
  
## Return Value  
 Pointer to the new toolbar; or `NULL` if a toolbar was not created.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)