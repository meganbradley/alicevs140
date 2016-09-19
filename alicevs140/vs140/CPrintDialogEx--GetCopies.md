---
title: "CPrintDialogEx::GetCopies"
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
ms.assetid: a74d7d4c-5f60-4535-b185-4636c7707456
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::GetCopies
Call this function after calling `DoModal` to retrieve the number of copies requested.  
  
## Syntax  
  
```  
  
int GetCopies( ) const;  
  
```  
  
## Return Value  
 The number of copies requested.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::PrintCollate](../vs140/CPrintDialogEx--PrintCollate.md)