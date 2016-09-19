---
title: "CMDIFrameWndEx::OnEraseMDIClientBackground"
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
ms.assetid: 971adfa2-0d93-40a6-8b74-b5f856088c84
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::OnEraseMDIClientBackground
Called by the framework when the MDI frame window processes a `WM_ERASEBKGND` message.  
  
## Syntax  
  
```  
virtual BOOL OnEraseMDIClientBackground(  
   CDC*    
);  
```  
  
## Return Value  
 `TRUE` if the application processes the message and erases the background.  
  
## Remarks  
 Override this member function if you want to process the `WM_ERASEBKGND` message in a `CMDIFrameWndEx`-derived class.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)