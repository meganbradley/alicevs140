---
title: "CArchive::Close"
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
ms.assetid: ff893d39-ccf9-4478-a5bd-6bb9101adfd8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::Close
Flushes any data remaining in the buffer, closes the archive, and disconnects the archive from the file.  
  
## Syntax  
  
```  
  
void Close( );  
```  
  
## Remarks  
 No further operations on the archive are permitted. After you close an archive, you can create another archive for the same file or you can close the file.  
  
 The member function **Close** ensures that all data is transferred from the archive to the file, and it makes the archive unavailable. To complete the transfer from the file to the storage medium, you must first use [CFile::Close](../vs140/CFile--Close.md) and then destroy the `CFile` object.  
  
## Example  
 See the example for [CArchive::WriteString](../vs140/CArchive--WriteString.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::Flush](../vs140/CArchive--Flush.md)   
 [CArchive::Abort](../vs140/CArchive--Abort.md)