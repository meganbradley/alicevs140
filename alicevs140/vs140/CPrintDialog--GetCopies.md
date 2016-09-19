---
title: "CPrintDialog::GetCopies"
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
ms.assetid: ff3c6e6c-333c-48e6-83f9-61961e0dd289
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::GetCopies
Retrieves the number of copies requested.  
  
## Syntax  
  
```  
  
int GetCopies( ) const;  
```  
  
## Return Value  
 The number of copies requested.  
  
## Remarks  
 Call this function after calling `DoModal` to retrieve the number of copies requested.  
  
## Example  
 See the example for [CPrintDialog::PrintCollate](../vs140/CPrintDialog--PrintCollate.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::PrintCollate](../vs140/CPrintDialog--PrintCollate.md)