---
title: "CWnd::ShowOwnedPopups"
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
ms.assetid: 0f7c9a14-5bbc-4e1e-b368-5bf4cb82e73e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ShowOwnedPopups
Shows or hides all pop-up windows owned by this window.  
  
## Syntax  
  
```  
  
      void ShowOwnedPopups(  
   BOOL bShow = TRUE   
);  
```  
  
#### Parameters  
 `bShow`  
 Specifies whether pop-up windows are to be shown or hidden. If this parameter is **TRUE**, all hidden pop-up windows are shown. If this parameter is **FALSE**, all visible pop-up windows are hidden.  
  
## Example  
 See the example for [CWnd::SetWindowPos](../vs140/CWnd--SetWindowPos.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [ShowOwnedPopups](http://msdn.microsoft.com/library/windows/desktop/ms633547)