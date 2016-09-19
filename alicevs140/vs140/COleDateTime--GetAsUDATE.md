---
title: "COleDateTime::GetAsUDATE"
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
ms.assetid: 4bbf0258-7f84-4b80-bc29-0afcf69022d9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::GetAsUDATE
Call this method to obtain the time in the `COleDateTime` object as a **UDATE** data structure.  
  
## Syntax  
  
```  
  
      bool GetAsUDATE(  
   UDATE& udate   
) const throw( );  
```  
  
#### Parameters  
 `udate`  
 A reference to a **UDATE** structure to receive the converted date/time value from the `COleDateTime` object.  
  
## Return Value  
 Returns **true** if successful; **false** if the conversion fails, or if the `COleDateTime` object is **NULL** or invalid.  
  
## Remarks  
 A **UDATE** structure represents an "unpacked" date.  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)