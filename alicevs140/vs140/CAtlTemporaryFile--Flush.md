---
title: "CAtlTemporaryFile::Flush"
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
ms.assetid: 95a48de1-6237-456c-b5f0-18d97dea19ff
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::Flush
Call this method to force any data remaining in the file buffer to be written to the temporary file.  
  
## Syntax  
  
```  
  
HRESULT Flush( ) throw( );  
  
```  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 Similar to [CAtlTemporaryFile::HandsOff](../vs140/CAtlTemporaryFile--HandsOff.md), except that the file is not closed.  
  
## Example  
 See the example for [CAtlTemporaryFile::CAtlTemporaryFile](../vs140/CAtlTemporaryFile--CAtlTemporaryFile.md).  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)