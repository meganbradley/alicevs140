---
title: "CControlBar::m_bAutoDelete"
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
ms.assetid: cd65807c-d555-4861-aae9-f69c59cee815
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::m_bAutoDelete
If nonzero, the `CControlBar` object is deleted when the Windows control bar is destroyed.  
  
## Syntax  
  
```  
  
BOOL m_bAutoDelete;  
  
```  
  
## Remarks  
 `m_bAutoDelete` is a public variable of type **BOOL**.  
  
 A control-bar object is usually embedded in a frame-window object. In this case, `m_bAutoDelete` is 0 because the embedded control-bar object is destroyed when the frame window is destroyed.  
  
 Set this variable to a nonzero value if you allocate a `CControlBar` object on the heap and you do not plan to call **delete**.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DestroyWindow](../vs140/CWnd--DestroyWindow.md)