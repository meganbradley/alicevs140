---
title: "CDockSite::FindPaneByID"
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
ms.assetid: 949ed90b-057d-4390-829c-0597739bcf29
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockSite::FindPaneByID
Returns the pane with the given ID.  
  
## Syntax  
  
```  
CPane* FindPaneByID(  
    UINT nID   
);  
```  
  
#### Parameters  
 [in] `nID`  
 The command ID of the pane to be found.  
  
## Return Value  
 A pointer to the pane with the specified command ID, or `NULL` if the pane is not found.  
  
## Remarks  
  
## Requirements  
 **Header:** afxDockSite.h  
  
## See Also  
 [CDockSite Class](../vs140/CDockSite-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)