---
title: "CPrintDialogEx::PrintCurrentPage"
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
ms.assetid: fa4724e5-7bed-4007-9e45-e0f3c9d677c5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::PrintCurrentPage
Call this function after calling `DoModal` to determine whether to print the current page in the document.  
  
## Syntax  
  
```  
  
BOOL PrintCurrentPage( ) const;  
  
```  
  
## Return Value  
 **TRUE** if **Print Current Page** is selected in the print dialog; otherwise **FALSE**.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::PrintAll](../vs140/CPrintDialogEx--PrintAll.md)   
 [CPrintDialogEx::PrintSelection](../vs140/CPrintDialogEx--PrintSelection.md)