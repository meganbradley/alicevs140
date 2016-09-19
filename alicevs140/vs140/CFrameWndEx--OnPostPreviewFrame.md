---
title: "CFrameWndEx::OnPostPreviewFrame"
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
ms.assetid: 7cbd3b92-118c-4ea5-af4e-2ea13a0bdbdb
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnPostPreviewFrame
Called by the framework when the user changes the print preview mode.  
  
## Syntax  
  
```  
afx_msg LRESULT OnPostPreviewFrame(  
   WPARAM wParam,  
   LPARAM lParam  
);  
```  
  
#### Parameters  
 [in] `wParam`  
 This parameter is not used.  
  
 [in] `lParam`  
 `TRUE` when the frame is in print preview mode; `FALSE` when print preview mode is off.  
  
## Return Value  
 Always returns 0.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)