---
title: "CAtlFile::SetSize"
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
ms.assetid: 1b2c1a48-a1de-432d-9406-3a70ef0bac1a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFile::SetSize
Call this method to set the size of the file.  
  
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
 Calls [SetFilePointer](http://msdn.microsoft.com/library/windows/desktop/aa365541) and [SetEndOfFile](http://msdn.microsoft.com/library/windows/desktop/aa365531) to set the size of the file. On return, the file pointer is positioned at the end of the file.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlFile Class](../vs140/CAtlFile-Class.md)   
 [CAtlFile::GetSize](../vs140/CAtlFile--GetSize.md)