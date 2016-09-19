---
title: "CPrintInfo::m_nJobNumber"
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
ms.assetid: e83aa3e2-7f23-4f0a-9be8-6abd6cb49e30
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::m_nJobNumber
Indicates the job number assigned by the operating system for the current print job.  
  
## Remarks  
 This value may be **SP_ERROR** if the job hasn't yet printed (that is, if the `CPrintInfo` object is newly constructed and has not yet been used to print), or if there was an error in starting the job.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)