---
title: "CAtlTemporaryFile::GetSize"
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
ms.assetid: 65fd00a6-8135-459e-a978-ceb4958c0fa5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::GetSize
Call this method to get the size in bytes of the temporary file.  
  
## Syntax  
  
```  
  
      HRESULT GetSize(  
   ULONGLONG& nLen   
) const throw( );  
```  
  
#### Parameters  
 `nLen`  
 The number of bytes in the file.  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)   
 [CAtlFile::GetSize](../vs140/CAtlFile--GetSize.md)   
 [CAtlTemporaryFile::SetSize](../vs140/CAtlTemporaryFile--SetSize.md)