---
title: "CFrameWndEx::OnPaneCheck"
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
ms.assetid: 591c392e-3dc1-4219-bd30-c13b07edd753
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnPaneCheck
Called by the framework to control the visibility of a pane.  
  
## Syntax  
  
```  
afx_msg BOOL OnPaneCheck(  
   UINT nID  
);  
```  
  
#### Parameters  
 [in] `nID`  
 Control ID of a pane.  
  
## Return Value  
 `TRUE` if the command was handled; `FALSE` to continue with command processing.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)