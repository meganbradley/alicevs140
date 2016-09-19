---
title: "CContainedWindowT::UnsubclassWindow"
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
ms.assetid: 4baa289b-6a73-4f5c-b4be-60e79a68d624
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContainedWindowT::UnsubclassWindow
Detaches the subclassed window from the `CContainedWindowT` object and restores the original window procedure, saved in [m_pfnSuperWindowProc](../vs140/CContainedWindowT--m_pfnSuperWindowProc.md).  
  
## Syntax  
  
```  
  
      HWND UnsubclassWindow(  
   BOOL bForce = FALSE  
);  
```  
  
#### Parameters  
 `bForce`  
 [in] Set to **TRUE** to force the original window procedure to be restored even if the window procedure for this `CContainedWindowT` object is not currently active. If `bForce` is set to **FALSE** and the window procedure for this `CContainedWindowT` object is not currently active, the original window procedure will not be restored.  
  
## Return Value  
 The handle to the window previously subclassed. If `bForce` is set to **FALSE** and the window procedure for this `CContainedWindowT` object is not currently active, returns **NULL**.  
  
## Remarks  
 Use this method only if you want to restore the original window procedure before the window is destroyed. Otherwise, [WindowProc](../vs140/CContainedWindowT--WindowProc.md) will automatically do this when the window is destroyed.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CContainedWindowT Class](../vs140/CContainedWindowT-Class.md)   
 [CContainedWindowT::SubclassWindow](../vs140/CContainedWindowT--SubclassWindow.md)