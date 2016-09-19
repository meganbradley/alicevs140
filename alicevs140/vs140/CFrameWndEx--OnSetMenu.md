---
title: "CFrameWndEx::OnSetMenu"
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
ms.assetid: f05251ce-b582-4a4a-b815-a5eeb0dab0e7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnSetMenu
Called by the framework to replace the frame window menu.  
  
## Syntax  
  
```  
afx_msg LRESULT OnSetMenu(  
   WPARAM wp,  
   LPARAM lp  
);  
BOOL OnSetMenu(  
   HMENU hmenu  
);  
```  
  
#### Parameters  
 [in] `wp`  
 Handle to the new frame window menu.  
  
 [in] `lp`  
 Handle to the new window menu.  
  
 [in] `hmenu`  
 Handle to the new frame window menu.  
  
## Return Value  
 `LRESULT` is the result from calling the default window procedure.  
  
 `BOOL` is `TRUE` if the event was handled; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)