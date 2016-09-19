---
title: "CFrameWnd::OnBarCheck"
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
ms.assetid: 8f530568-1570-4ac2-8606-3b3fe52e74a7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::OnBarCheck
Called whenever an action is performed on the specified control bar.  
  
## Syntax  
  
```  
  
      afx_msg BOOL OnBarCheck(  
   UINT nID  
);  
```  
  
#### Parameters  
 `nID`  
 The ID of the control bar being shown.  
  
## Return Value  
 Nonzero if the control bar existed; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)