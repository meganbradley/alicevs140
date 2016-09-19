---
title: "CLongBinary::m_dwDataLength"
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
ms.assetid: ef3e9471-1a3b-49a7-92e8-5f29ded135b2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLongBinary::m_dwDataLength
Stores the actual size in bytes of the data stored in the `HGLOBAL` handle in `m_hData`.  
  
## Syntax  
  
```  
  
SQLULEN m_dwDataLength;  
  
```  
  
## Remarks  
 This size may be smaller than the size of the memory block allocated for the data. Call the Win32 [GLobalSize](http://msdn.microsoft.com/library/windows/desktop/aa366593) function to get the allocated size.  
  
## Requirements  
 **Header:** afxdb_.h  
  
## See Also  
 [CLongBinary Class](../vs140/CLongBinary-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)