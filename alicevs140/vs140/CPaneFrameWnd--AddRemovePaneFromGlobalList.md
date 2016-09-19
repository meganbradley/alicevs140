---
title: "CPaneFrameWnd::AddRemovePaneFromGlobalList"
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
ms.assetid: b9d35c4a-8a7a-46a6-bea7-110ed52c37f4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::AddRemovePaneFromGlobalList
Adds or removes a pane from the global list.  
  
## Syntax  
  
```  
static BOOL __stdcall AddRemovePaneFromGlobalList(  
   CBasePane* pWnd,  
   BOOL bAdd  
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 The pane to add or remove.  
  
 [in] `bAdd`  
 If non-zero, add the pane. If 0, remove the pane.  
  
## Return Value  
 Nonzero if the method was successful; otherwise 0.  
  
## Requirements  
 **Header:** afxpaneframewnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)