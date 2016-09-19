---
title: "CFrameWndEx::OnGetMinMaxInfo"
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
ms.assetid: c8f33a54-98e3-4bdf-9a6d-c78c4d39d7fb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnGetMinMaxInfo
Called by the framework when the frame is resized to set window dimension limits.  
  
## Syntax  
  
```  
afx_msg void OnGetMinMaxInfo(  
   MINMAXINFO FAR* lpMMI  
);  
```  
  
#### Parameters  
 [in] `lpMMI`  
 Pointer to a [MINMAXINFO](http://msdn.microsoft.com/library/windows/desktop/ms632605) structure.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)