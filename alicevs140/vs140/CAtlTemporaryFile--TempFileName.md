---
title: "CAtlTemporaryFile::TempFileName"
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
ms.assetid: 0d4095d9-99f0-40c0-9567-030ce7ce3197
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::TempFileName
Call this method to return the name of temporary file.  
  
## Syntax  
  
```  
  
LPCTSTR TempFileName( ) throw( );  
  
```  
  
## Return Value  
 Returns the `LPCTSTR` pointing to the file name.  
  
## Remarks  
 The file name is generated in [CAtlTemporaryFile::CAtlTemporaryFile](../vs140/CAtlTemporaryFile--CAtlTemporaryFile.md) with a call to the [GetTempFile](http://msdn.microsoft.com/library/windows/desktop/aa364991)[!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] function. The file extension will always be "TFR" for the temporary file.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)