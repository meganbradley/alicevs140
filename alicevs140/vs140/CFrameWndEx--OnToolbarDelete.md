---
title: "CFrameWndEx::OnToolbarDelete"
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
ms.assetid: 962588f9-6252-464b-8df1-17809e0a8d6b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnToolbarDelete
Called by the framework when a toolbar is deleted.  
  
## Syntax  
  
```  
afx_msg LRESULT OnToolbarDelete(  
   WPARAM,  
   LPARAM lp  
);  
```  
  
#### Parameters  
 [in]  
 This parameter is not used.  
  
 [in] `lp`  
 Pointer to a toolbar.  
  
## Return Value  
 `TRUE` if the toolbar was deleted; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)