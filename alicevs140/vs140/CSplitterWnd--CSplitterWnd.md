---
title: "CSplitterWnd::CSplitterWnd"
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
ms.assetid: 8c5618f1-e97b-4128-aa6a-9b4810086004
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::CSplitterWnd
Call to construct a `CSplitterWnd` object.  
  
## Syntax  
  
```  
  
CSplitterWnd( );  
```  
  
## Remarks  
 Construct a `CSplitterWnd` object in two steps. First, call the constructor, which creates the `CSplitterWnd` object, and then call the [Create](../vs140/CSplitterWnd--Create.md) member function, which creates the splitter window and attaches it to the `CSplitterWnd` object.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::Create](../vs140/CSplitterWnd--Create.md)