---
title: "CAtlTemporaryFile::SetSize"
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
ms.assetid: 0b866546-7493-4ce5-aea1-7f475fa8ad05
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::SetSize
Call this method to set the size of the temporary file.  
  
## Syntax  
  
```  
  
      HRESULT SetSize(  
   ULONGLONG nNewLen   
) throw( );  
```  
  
#### Parameters  
 `nNewLen`  
 The new length of the file in bytes.  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 Calls [CAtlFile::SetSize](../vs140/CAtlFile--SetSize.md). On return, the file pointer is positioned at the end of the file.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)   
 [CAtlTemporaryFile::GetSize](../vs140/CAtlTemporaryFile--GetSize.md)