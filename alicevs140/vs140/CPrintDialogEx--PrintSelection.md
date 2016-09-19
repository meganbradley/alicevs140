---
title: "CPrintDialogEx::PrintSelection"
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
ms.assetid: 9327f163-9f99-4edd-b0a9-adf6fb3d24a1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::PrintSelection
Call this function after calling `DoModal` to determine whether to print only the currently selected items.  
  
## Syntax  
  
```  
  
BOOL PrintSelection( ) const;  
  
```  
  
## Return Value  
 **TRUE** if only the selected items are to be printed; otherwise **FALSE**.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::PrintAll](../vs140/CPrintDialogEx--PrintAll.md)   
 [CPrintDialogEx::PrintRange](../vs140/CPrintDialogEx--PrintRange.md)