---
title: "CWnd::ReleaseDC"
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
ms.assetid: d5e52d65-c5a8-42bd-81d0-82443a5f8fe5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ReleaseDC
Releases a device context, freeing it for use by other applications.  
  
## Syntax  
  
```  
  
      int ReleaseDC(  
   CDC* pDC   
);  
```  
  
#### Parameters  
 `pDC`  
 Identifies the device context to be released.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The effect of the `ReleaseDC` member function depends on the device-context type.  
  
 The application must call the `ReleaseDC` member function for each call to the [GetWindowDC](../vs140/CWnd--GetWindowDC.md) member function and for each call to the [GetDC](../vs140/CWnd--GetDC.md) member function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDC](../vs140/CWnd--GetDC.md)   
 [CWnd::GetWindowDC](../vs140/CWnd--GetWindowDC.md)   
 [ReleaseDC](http://msdn.microsoft.com/library/windows/desktop/dd162920)