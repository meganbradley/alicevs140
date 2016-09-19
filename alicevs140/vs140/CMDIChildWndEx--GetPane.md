---
title: "CMDIChildWndEx::GetPane"
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
ms.assetid: d1ff003d-8f8d-43e8-b5df-f689224ef0d7
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::GetPane
Finds a pane by the specified control ID.  
  
## Syntax  
  
```  
CBasePane* GetPane(  
   UINT nID  
);  
```  
  
#### Parameters  
 [in] `nID`  
 The control ID of the pane to find.  
  
## Return Value  
 A pointer to the pane if found, otherwise `NULL`.  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)