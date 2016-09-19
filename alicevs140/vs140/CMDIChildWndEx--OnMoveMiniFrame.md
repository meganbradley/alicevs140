---
title: "CMDIChildWndEx::OnMoveMiniFrame"
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
ms.assetid: fb774296-99e6-4193-a3e0-f9e431e27dfd
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::OnMoveMiniFrame
Called by the framework to move a mini-frame window.  
  
## Syntax  
  
```  
virtual BOOL OnMoveMiniFrame(  
   CWnd* pFrame  
);  
```  
  
#### Parameters  
 [in] `pFrame`  
 A pointer to a mini-frame window.  
  
## Return Value  
 `TRUE` if the method succeeds, otherwise `FALSE`.  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)