---
title: "CMDIFrameWndEx::GetPane"
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
ms.assetid: 8e449957-62f9-43af-bb81-7461a361b019
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::GetPane
Returns a pointer to the pane that has the specified control ID.  
  
## Syntax  
  
```  
CBasePane* GetPane(  
   UINT nID   
);  
```  
  
#### Parameters  
 [in] `nID`  
 The control ID.  
  
## Return Value  
 A pointer to the pane that has the specified control ID, if it exists. Otherwise, `NULL`.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)