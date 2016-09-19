---
title: "CFrameWndEx::OnSetText"
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
ms.assetid: 3aca8d5c-2c36-46a6-a644-1478536f470f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnSetText
Called by the framework to set the text of a window.  
  
## Syntax  
  
```  
afx_msg LRESULT OnSetText(  
   WPARAM wParam,  
   LPARAM lParam  
);  
```  
  
#### Parameters  
 [in] `wParam`  
 This parameter is not used.  
  
 [in] `lParam`  
 Pointer to the text for the window.  
  
## Return Value  
 Return value from a call to [DefWindowProc](http://msdn.microsoft.com/library/windows/desktop/ms633572).  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)