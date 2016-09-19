---
title: "CBasePane::GetPaneIcon"
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
ms.assetid: 192a01d7-1fd9-4cb8-98cc-ab04e221d223
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::GetPaneIcon
Returns a handle to the pane icon.  
  
## Syntax  
  
```  
virtual HICON GetPaneIcon(  
   BOOL bBigIcon  
);  
```  
  
#### Parameters  
 [in] `bBigIcon`  
 Specifies a 32 pixel by 32 pixel icon if `TRUE`; specifies a 16 pixel by 16 pixel icon if `FALSE`.  
  
## Return Value  
 A handle to the pane icon. If unsuccessful, returns `NULL`.  
  
## Remarks  
 The default implementation calls [CWnd::GetIcon](../vs140/CWnd--GetIcon.md).  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)