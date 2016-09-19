---
title: "CFrameWndEx::WinHelp"
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
ms.assetid: 9c8652fb-c1b0-4bb4-8376-7264df2d05a9
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::WinHelp
Invokes either the WinHelp application or context related help.  
  
## Syntax  
  
```  
virtual void WinHelp(  
   DWORD dwData,  
   UINT nCmd = HELP_CONTEXT  
);  
```  
  
#### Parameters  
 `dwData`  
 Data that depends on the `nCmd` parameter. For a list of possible values see [WinHelp](http://msdn.microsoft.com/library/windows/desktop/bb762267).  
  
 `nCmd`  
 The help command. For a list of possible values see [WinHelp](http://msdn.microsoft.com/library/windows/desktop/bb762267).  
  
## Remarks  
  
## Requirements  
 **Header:**  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)