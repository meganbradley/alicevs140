---
title: "FILETIME Structure"
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
ms.topic: article
ms.assetid: e09557e2-b6d7-4dd5-a5b9-6328bca88595
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FILETIME Structure
The `FILETIME` structure is a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601.  
  
## Syntax  
  
```  
  
      typedef struct _FILETIME {  
   DWORD dwLowDateTime;   /* low 32 bits  */  
   DWORD dwHighDateTime;  /* high 32 bits */  
} FILETIME, *PFILETIME, *LPFILETIME;  
```  
  
#### Parameters  
 *dwLowDateTime*  
 Specifies the low 32 bits of the file time.  
  
 *dwHighDateTime*  
 Specifies the high 32 bits of the file time.  
  
## Requirements  
 **Header:** windef.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [CTime::CTime](../Topic/CTime::CTime.md)