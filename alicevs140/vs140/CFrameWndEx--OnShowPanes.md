---
title: "CFrameWndEx::OnShowPanes"
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
ms.assetid: 7cb6286e-8e37-4044-8644-13d2052cfc88
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnShowPanes
Called by the framework to show or hide panes.  
  
## Syntax  
  
```  
virtual BOOL OnShowPanes(  
   BOOL bShow  
);  
```  
  
#### Parameters  
 [in] `bShow`  
 `TRUE` if the application shows the panes; `FALSE` otherwise.  
  
## Return Value  
 This method always return `FALSE`.  
  
## Remarks  
 The default implementation shows the panes if `bShow` is `TRUE` and the panes are hidden or when `bShow` is `FALSE` and the panes are visible.  
  
 The default implementation hides the panes if `bShow` is `TRUE` and the panes are visible or when `bShow` is `FALSE` and the panes are hidden.  
  
 Override this method in a derived class to execute custom code when the framework shows or hides panes.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)