---
title: "CDC::GetMiterLimit"
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
ms.assetid: 63eaa0c2-9ae9-4d9b-bd37-455260c2ee11
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetMiterLimit
Returns the miter limit for the device context.  
  
## Syntax  
  
```  
  
float GetMiterLimit( ) const;  
```  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The miter limit is used when drawing geometric lines that have miter joins.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetMiterLimit](../vs140/CDC--SetMiterLimit.md)   
 [GetMiterLimit](http://msdn.microsoft.com/library/windows/desktop/dd144900)