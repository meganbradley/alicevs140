---
title: "&lt;PAVE OVER&gt; AFX_GLOBAL_DATA::DwmExtendFrameIntoClientArea"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3c7cbec7-c80d-4933-a531-b99e44295ed6
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; AFX_GLOBAL_DATA::DwmExtendFrameIntoClientArea
Provides a simple way to call the Windows [DwmExtendFrameIntoClientArea](http://msdn.microsoft.com/library/windows/desktop/aa969512) method.  
  
## Syntax  
  
```  
BOOL DwmExtendFrameIntoClientArea(  
   HWND hWnd,   
   AFX_MARGINS* pMargins  
);  
```  
  
#### Parameters  
 [in] `hWnd`  
 The handle to a window whose frame is extended behind the client area.  
  
 [in] `pMargins`  
 A pointer to a structure that describes the margins to use when extending the frame into the client area. The members of the `AFX_MARGINS` structure are identical to the members of the [MARGINS](http://msdn.microsoft.com/library/windows/desktop/bb773244) structure.  
  
## Return Value  
 `TRUE` if this method is successful; otherwise, `FALSE`.  
  
## Remarks  
 This method extends the window frame behind the client area.  
  
## Requirements  
 **Header:** afxglobals.h  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)