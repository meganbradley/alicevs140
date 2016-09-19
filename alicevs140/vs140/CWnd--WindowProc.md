---
title: "CWnd::WindowProc"
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
ms.assetid: 81390b70-464e-4289-898c-c1ab617e7662
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::WindowProc
Provides a Windows procedure (`WindowProc`) for a `CWnd` object.  
  
## Syntax  
  
```  
  
      virtual LRESULT WindowProc(  
   UINT message,  
   WPARAM wParam,  
   LPARAM lParam   
);  
```  
  
#### Parameters  
 `message`  
 Specifies the Windows message to be processed.  
  
 `wParam`  
 Provides additional information used in processing the message. The parameter value depends on the message.  
  
 `lParam`  
 Provides additional information used in processing the message. The parameter value depends on the message.  
  
## Return Value  
 The return value depends on the message.  
  
## Remarks  
 It dispatches messages through the window's message map.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)