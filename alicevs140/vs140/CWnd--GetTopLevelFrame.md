---
title: "CWnd::GetTopLevelFrame"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: c2646ce9-50d3-4806-8b6e-bab7220c9f7d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetTopLevelFrame
Call this member function to retrieve the window's top level frame window, if any.  
  
## Syntax  
  
```  
  
CFrameWnd* GetTopLevelFrame( ) const;  
  
```  
  
## Return Value  
 Identifies the top-level frame window of the window.  
  
 The returned pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 If `CWnd` has no attached window, or its top-level parent is not a [CFrameWnd](../vs140/CFrameWnd-Class.md)-derived object, this function returns **NULL**.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetTopLevelOwner](../vs140/CWnd--GetTopLevelOwner.md)   
 [CWnd::GetTopLevelParent](../vs140/CWnd--GetTopLevelParent.md)