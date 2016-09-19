---
title: "CMDIFrameWndEx::CreateNewWindow"
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
ms.assetid: 71c421a5-e296-4795-9315-d544af8f1fff
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::CreateNewWindow
Called by the framework to create a new window.  
  
## Syntax  
  
```  
virtual CMDIChildWndEx* CreateNewWindow(  
   LPCTSTR lpcszDocName,  
   CObject* pObj  
);  
```  
  
#### Parameters  
 [in] `lpcszDocName`  
 The document name.  
  
 [in] `pObj`  
 Reserved for future use.  
  
## Return Value  
 A pointer to the new window.  
  
## Requirements  
 **Header:** afxmdiframewndex.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)