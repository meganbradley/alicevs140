---
title: "CFile::Flush"
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
ms.assetid: 5061b688-6abe-4513-b08b-4973b3699963
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::Flush
Forces any data remaining in the file buffer to be written to the file.  
  
## Syntax  
  
```  
  
virtual void Flush( );  
```  
  
## Remarks  
 The use of `Flush` does not guarantee flushing of `CArchive` buffers. If you are using an archive, call [CArchive::Flush](../vs140/CArchive--Flush.md) first.  
  
## Example  
 See the example for [CFile::SetFilePath](../vs140/CFile--SetFilePath.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)