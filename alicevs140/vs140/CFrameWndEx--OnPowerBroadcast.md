---
title: "CFrameWndEx::OnPowerBroadcast"
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
ms.assetid: cbcf7398-d896-4d8c-8f04-9d9789f50933
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnPowerBroadcast
Called by the framework when a power management event occurs.  
  
## Syntax  
  
```  
afx_msg LRESULT OnPowerBroadcast(  
   WPARAM wp,  
   LPARAM lp  
);  
```  
  
#### Parameters  
 [in] `wp`  
 The power management event. For a list of possible values see [WM_POWERBROADCAST Message](http://msdn.microsoft.com/library/windows/desktop/aa373247).  
  
 [in] `lp`  
 This parameter is not used.  
  
## Return Value  
 Result from calling the default window procedure.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)