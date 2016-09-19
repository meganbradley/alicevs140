---
title: "&lt;PAVE OVER&gt; AFX_GLOBAL_DATA::DwmDefWindowProc"
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
ms.assetid: e589d5dc-ee4c-40ea-9772-f7f2e2789ae4
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; AFX_GLOBAL_DATA::DwmDefWindowProc
Provides a simple way to call the Windows [DwmDefWindowProc](http://msdn.microsoft.com/library/windows/desktop/aa969507) method.  
  
## Syntax  
  
```  
LRESULT DwmDefWindowProc(  
   HWND hWnd,   
   UINT message,   
   WPARAM wp,   
   LPARAM lp  
);  
```  
  
#### Parameters  
 [in] `hWnd`  
 Handle to the window procedure that received the message.  
  
 [in] `message`  
 Specifies the message.  
  
 [in] `wp`  
 Specifies additional message information. The content of this parameter depends on the value of the `message` parameter.  
  
 [in] `lp`  
 Specifies additional message information. The content of this parameter depends on the value of the `message` parameter.  
  
## Return Value  
 The result of the hit test.  
  
## Remarks  
 This method enables [Desktop Window Manager](http://msdn.microsoft.com/library/windows/desktop/aa969540) (DWM) hit-testing within the non-client area when it is called with the [WM_NCHITTEST](http://msdn.microsoft.com/library/windows/desktop/ms645618) notification.  
  
## Requirements  
 **Header:** afxglobals.h  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)