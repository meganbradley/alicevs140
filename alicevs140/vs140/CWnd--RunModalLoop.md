---
title: "CWnd::RunModalLoop"
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
ms.assetid: 20563fad-e9d3-4b35-9d70-65918f44c6e5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::RunModalLoop
Call this member function to retrieve, translate, or dispatch messages until [ContinueModal](../vs140/CWnd--ContinueModal.md) returns **FALSE**.  
  
## Syntax  
  
```  
  
      int RunModalLoop(  
   DWORD dwFlags = 0   
);  
```  
  
#### Parameters  
 `dwFlags`  
 Specifies the Windows message to be sent. Can be one of the following values:  
  
-   **MLF_NOIDLEMSG** Don't send [WM_ENTERIDLE](http://msdn.microsoft.com/library/windows/desktop/ms645422) messages to the parent.  
  
-   **MLF_NOKICKIDLE** Don't send **WM_KICKIDLE** messages to the window.  
  
-   **MLF_SHOWONIDLE** Show the window when message queue goes idle.  
  
## Return Value  
 Specifies the value of the `nResult` parameter passed to the [EndModalLoop](../vs140/CWnd--EndModalLoop.md) member function, which is then used to end the modal loop.  
  
## Remarks  
 By default, `ContinueModal` returns **FALSE** after `EndModalLoop` is called. Returns the value provided as `nResult` to `EndModalLoop`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::EndModalLoop](../vs140/CWnd--EndModalLoop.md)   
 [WM_ENTERIDLE](http://msdn.microsoft.com/library/windows/desktop/ms645422)