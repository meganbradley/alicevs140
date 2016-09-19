---
title: "CPrintDialogEx::PrintAll"
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
ms.assetid: cd91dc57-bc95-49fd-863b-ebdc8a7cbe27
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::PrintAll
Call this function after calling `DoModal` to determine whether to print all pages in the document.  
  
## Syntax  
  
```  
  
BOOL PrintAll( ) const;  
  
```  
  
## Return Value  
 **TRUE** if all pages in the document are to be printed; otherwise **FALSE**.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::PrintCurrentPage](../vs140/CPrintDialogEx--PrintCurrentPage.md)   
 [CPrintDialogEx::PrintRange](../vs140/CPrintDialogEx--PrintRange.md)   
 [CPrintDialogEx::PrintSelection](../vs140/CPrintDialogEx--PrintSelection.md)