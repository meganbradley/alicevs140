---
title: "CPaneFrameWnd::m_bUseSaveBits"
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
ms.assetid: 9cc5f00e-d3f8-47a3-bc5a-c54f115dd7e3
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::m_bUseSaveBits
Specifies whether to register the window class that has the `CS_SAVEBITS` class style.  
  
## Syntax  
  
```  
AFX_IMPORT_DATA static BOOL m_bUseSaveBits;  
```  
  
## Remarks  
 Set this static member to `TRUE` to register the mini-frame window class that has the `CS_SAVEBITS` style. This may help reduce flickering when a user drags the mini-frame window.  
  
## Requirements  
 **Header:** afxPaneFrameWnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)