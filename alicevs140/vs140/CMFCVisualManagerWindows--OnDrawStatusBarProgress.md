---
title: "CMFCVisualManagerWindows::OnDrawStatusBarProgress"
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
ms.assetid: 7f9a0115-a207-4be1-a32c-a005aaca7126
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerWindows::OnDrawStatusBarProgress
[!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
## Syntax  
  
```  
virtual void OnDrawStatusBarProgress(  
   CDC* pDC,  
   CMFCStatusBar* pStatusBar,  
   CRect rectProgress,  
   int nProgressTotal,  
   int nProgressCurr,  
   COLORREF clrBar,  
   COLORREF clrProgressBarDest,  
   COLORREF clrProgressText,  
   BOOL bProgressText  
);  
```  
  
#### Parameters  
 [in] `pDC`  
  [in] `pStatusBar`  
  [in] `rectProgress`  
  [in] `nProgressTotal`  
  [in] `nProgressCurr`  
  [in] `clrBar`  
  [in] `clrProgressBarDest`  
  [in] `clrProgressText`  
  [in] `bProgressText`  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanagerwindows.h  
  
## See Also  
 [CMFCVisualManagerWindows Class](../vs140/CMFCVisualManagerWindows-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)