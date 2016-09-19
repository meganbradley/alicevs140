---
title: "CPrintDialogEx::PrintCollate"
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
ms.assetid: c43342bd-e847-4c63-9916-1f020ec57d2a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::PrintCollate
Call this function after calling `DoModal` to determine whether the printer should collate all printed copies of the document.  
  
## Syntax  
  
```  
  
BOOL PrintCollate( ) const;  
  
```  
  
## Return Value  
 **TRUE** if the user selects the collate check box in the dialog box; otherwise **FALSE**.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::GetCopies](../vs140/CPrintDialogEx--GetCopies.md)