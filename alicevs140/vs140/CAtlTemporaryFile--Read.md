---
title: "CAtlTemporaryFile::Read"
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
ms.assetid: 96d1c3dd-d84a-4cb5-bf15-cc55005b12bb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::Read
Call this method to read data from the temporary file starting at the position indicated by the file pointer.  
  
## Syntax  
  
```  
  
      HRESULT Read(  
   LPVOID pBuffer,  
   DWORD nBufSize,  
   DWORD& nBytesRead   
) throw( );  
```  
  
#### Parameters  
 `pBuffer`  
 Pointer to the buffer that will receive the data read from the file.  
  
 `nBufSize`  
 The buffer size in bytes.  
  
 `nBytesRead`  
 The number of bytes read.  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 Calls [CAtlFile::Read](../vs140/CAtlFile--Read.md). To change the position of the file pointer, call [CAtlTemporaryFile::Seek](../vs140/CAtlTemporaryFile--Seek.md).  
  
## Example  
 See the example for [CAtlTemporaryFile::CAtlTemporaryFile](../vs140/CAtlTemporaryFile--CAtlTemporaryFile.md).  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)   
 [CAtlTemporaryFile::Write](../vs140/CAtlTemporaryFile--Write.md)