---
title: "CAtlTemporaryFile::Seek"
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
ms.assetid: d08c6183-25b1-4175-ad73-458fc323f935
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::Seek
Call this method to move the file pointer of the temporary file.  
  
## Syntax  
  
```  
  
      HRESULT Seek(  
   LONGLONG nOffset,  
   DWORD dwFrom = FILE_CURRENT   
) throw( );  
```  
  
#### Parameters  
 `nOffset`  
 The offset, in bytes, from the starting point given by *dwFrom.*  
  
 `dwFrom`  
 The starting point (FILE_BEGIN, FILE_CURRENT, or FILE_END).  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 Calls [CAtlFile::Seek](../vs140/CAtlFile--Seek.md). To obtain the current file pointer position, call [CAtlTemporaryFile::GetPosition](../vs140/CAtlTemporaryFile--GetPosition.md).  
  
## Example  
 See the example for [CAtlTemporaryFile::CAtlTemporaryFile](../vs140/CAtlTemporaryFile--CAtlTemporaryFile.md).  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)   
 [CAtlTemporaryFile::Read](../vs140/CAtlTemporaryFile--Read.md)