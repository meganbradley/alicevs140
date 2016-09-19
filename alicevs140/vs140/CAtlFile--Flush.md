---
title: "CAtlFile::Flush"
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
ms.assetid: 8dd6ec7a-0081-47cd-aa78-1a97cbb42784
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFile::Flush
Call this method to clear the buffers for the file and cause all buffered data to be written to the file.  
  
## Syntax  
  
```  
  
HRESULT Flush( ) throw( );  
  
```  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 Calls [FlushFileBuffers](http://msdn.microsoft.com/library/windows/desktop/aa364439) to flush buffered data to the file.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlFile Class](../vs140/CAtlFile-Class.md)