---
title: "CAtlFile::UnlockRange"
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
ms.assetid: c327b8eb-2b62-4113-b542-e9e25c8b8ff1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFile::UnlockRange
Call this method to unlock a region of the file.  
  
## Syntax  
  
```  
  
      HRESULT UnlockRange(  
   ULONGLONG nPos,  
   ULONGLONG nCount   
) throw( );  
```  
  
#### Parameters  
 `nPos`  
 The position in the file where the unlock should begin.  
  
 `nCount`  
 The length of the byte range to be unlocked.  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 Calls [UnlockFile](http://msdn.microsoft.com/library/windows/desktop/aa365715) to unlock a region of the file.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlFile Class](../vs140/CAtlFile-Class.md)   
 [CAtlFile::LockRange](../vs140/CAtlFile--LockRange.md)