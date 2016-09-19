---
title: "CFrameWndEx::GetPane"
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
ms.assetid: 17e1e36f-bbe0-443c-9c7a-50745986b49c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::GetPane
Returns a pointer to the pane that has the specified ID.  
  
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
 A pointer to the pane that has the specified ID. `NULL` if no such pane exists.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)