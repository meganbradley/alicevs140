---
title: "CAtlFile::Write"
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
ms.assetid: 135cebb6-a01f-41e0-8fae-44aeaee8e4fb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFile::Write
Call this method to write data to the file starting at the position indicated by the file pointer.  
  
## Syntax  
  
```  
  
      HRESULT Write(  
   LPCVOID pBuffer,  
   DWORD nBufSize,  
   LPOVERLAPPED pOverlapped,  
   LPOVERLAPPED_COMPLETION_ROUTINE pfnCompletionRoutine   
) throw( );  
HRESULT Write(  
   LPCVOID pBuffer,  
   DWORD nBufSize,  
   DWORD* pnBytesWritten = NULL   
) throw( );  
HRESULT Write(  
   LPCVOID pBuffer,  
   DWORD nBufSize,  
   LPOVERLAPPED pOverlapped   
) throw( );  
```  
  
#### Parameters  
 `pBuffer`  
 The buffer containing the data to be written to the file.  
  
 `nBufSize`  
 The number of bytes to be transferred from the buffer.  
  
 `pOverlapped`  
 The overlapped structure. See `lpOverlapped` in [WriteFile](http://msdn.microsoft.com/library/windows/desktop/aa365747) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pfnCompletionRoutine`  
 The completion routine. See *lpCompletionRoutine* in [WriteFileEx](http://msdn.microsoft.com/library/windows/desktop/aa365748) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pnBytesWritten`  
 The bytes written.  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 The first three forms call [WriteFile](http://msdn.microsoft.com/library/windows/desktop/aa365747), the last calls [WriteFileEx](http://msdn.microsoft.com/library/windows/desktop/aa365748) to write data to the file. Use [CAtlFile::Seek](../vs140/CAtlFile--Seek.md) to move the file pointer.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlFile Class](../vs140/CAtlFile-Class.md)   
 [CAtlFile::Read](../vs140/CAtlFile--Read.md)