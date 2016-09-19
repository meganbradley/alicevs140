---
title: "CFrameWndEx::OnUpdateFrameTitle"
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
ms.assetid: 9df9d104-d8a7-4af2-91e3-dcf393a258d2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnUpdateFrameTitle
The framework calls this method to update the title bar of the frame window.  
  
## Syntax  
  
```  
virtual void OnUpdateFrameTitle(  
   BOOL bAddToTitle  
);  
```  
  
#### Parameters  
 [in] `bAddToTitle`  
 `TRUE` to add the active document title to the frame window title bar; otherwise `FALSE.`  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)