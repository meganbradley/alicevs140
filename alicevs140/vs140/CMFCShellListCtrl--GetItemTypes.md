---
title: "CMFCShellListCtrl::GetItemTypes"
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
ms.assetid: 0d7b0319-12df-4565-a70d-3032fadb8d85
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCShellListCtrl::GetItemTypes
Returns the type of items displayed by the [CMFCShellListCtrl](../vs140/CMFCShellListCtrl-Class.md) object.  
  
## Syntax  
  
```  
SHCONTF GetItemTypes() const;  
```  
  
## Return Value  
 A [SHCONTF](http://msdn.microsoft.com/library/windows/desktop/bb762539) value that contains the type of items listed in the `CMFCShellListCtrl`.  
  
## Remarks  
 To set the type of items listed in a `CMFCShellListCtrl`, call [CMFCShellListCtrl::SetItemTypes](../vs140/CMFCShellListCtrl--SetItemTypes.md).  
  
## Requirements  
 **Header:** afxshelllistctrl.h  
  
## See Also  
 [CMFCShellListCtrl Class](../vs140/CMFCShellListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCShellListCtrl::SetItemTypes](../vs140/CMFCShellListCtrl--SetItemTypes.md)