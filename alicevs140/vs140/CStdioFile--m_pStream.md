---
title: "CStdioFile::m_pStream"
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
ms.assetid: 706de778-4f04-4518-a692-d4a434a28f2a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStdioFile::m_pStream
The `m_pStream` data member is the pointer to an open file as returned by the C run-time function `fopen`.  
  
## Syntax  
  
```  
  
FILE* m_pStream;  
  
```  
  
## Remarks  
 It is **NULL** if the file has never been opened or has been closed.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CStdioFile Class](../vs140/CStdioFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)