---
title: "CAtlFile::GetSize"
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
ms.assetid: 8334a5e5-7cd8-4857-90db-77893c726439
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFile::GetSize
Call this method to get the size in bytes of the file.  
  
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
  
## Remarks  
 Calls [GetFileSize](http://msdn.microsoft.com/library/windows/desktop/aa364955) to get the size in bytes of the file.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlFile Class](../vs140/CAtlFile-Class.md)   
 [CAtlFile::GetPosition](../vs140/CAtlFile--GetPosition.md)   
 [CAtlFile::SetSize](../vs140/CAtlFile--SetSize.md)