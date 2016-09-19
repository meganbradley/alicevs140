---
title: "CSplitterWnd::DoKeyboardSplit"
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
ms.assetid: 6735e721-171b-4211-b478-96a1ab19b507
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::DoKeyboardSplit
Performs the keyboard split command, usually "Window Split."  
  
## Syntax  
  
```  
  
virtual BOOL DoKeyboardSplit( );  
  
```  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function is a high level command that is used by the [CView](../vs140/CView-Class.md) class to delegate to the `CSplitterWnd` implementation.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView Class](../vs140/CView-Class.md)