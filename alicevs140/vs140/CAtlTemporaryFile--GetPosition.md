---
title: "CAtlTemporaryFile::GetPosition"
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
ms.assetid: 8ee6f550-0380-4a43-86e0-e187e3e7eaeb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::GetPosition
Call this method to get the current file pointer position.  
  
## Syntax  
  
```  
  
      HRESULT GetPosition(  
   ULONGLONG& nPos   
) const throw( );  
```  
  
#### Parameters  
 `nPos`  
 The position in bytes.  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 To change the file pointer position, use [CAtlTemporaryFile::Seek](../vs140/CAtlTemporaryFile--Seek.md).  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)   
 [CAtlFile::GetPosition](../vs140/CAtlFile--GetPosition.md)