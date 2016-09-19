---
title: "CFrameWndEx::OnNcCalcSize"
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
ms.assetid: 0f2f06f8-096f-40b4-9b04-b70e52ead0b4
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnNcCalcSize
Called by the framework when the size and position of the client area must be calculated.  
  
## Syntax  
  
```  
afx_msg void OnNcCalcSize(  
   BOOL bCalcValidRects,  
   NCCALCSIZE_PARAMS FAR* lpncsp  
);  
```  
  
#### Parameters  
 [in] `bCalcValidRects`  
 `TRUE` when the application must specify a valid client area; otherwise, `FALSE`.  
  
 [in] `lpncsp`  
 Pointer to a `NCCALCSIZE_PARAMS` structure that contains frame dimension changes.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)