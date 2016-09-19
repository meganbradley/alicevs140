---
title: "Path Field Limits"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2b5d0e43-1347-45b4-8397-24a8a45c444e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Path Field Limits
## Syntax  
  
```  
#include <stdlib.h>  
```  
  
## Remarks  
 These constants define the maximum length for the path and for the individual fields within the path.  
  
|Constant|Meaning|  
|--------------|-------------|  
|`_MAX_DIR`|Maximum length of directory component|  
|`_MAX_DRIVE`|Maximum length of drive component|  
|`_MAX_EXT`|Maximum length of extension component|  
|`_MAX_FNAME`|Maximum length of filename component|  
|`_MAX_PATH`|Maximum length of full path|  
  
> [!NOTE]
>  The C Runtime supports path lengths up to 32768 characters in length, but it is up to the operating system, specifically the file system, to support these longer paths. The sum of the fields should not exceed `_MAX_PATH` for full backwards compatibility with FAT32 file systems. [!INCLUDE[win2kfamily](../vs140/includes/win2kfamily_md.md)], [!INCLUDE[WinXpFamily](../vs140/includes/winxpfamily_md.md)], [!INCLUDE[WinXPSvr](../vs140/includes/winxpsvr_md.md)], and Windows Vista NTFS file system supports paths up to 32768 characters in length, but only when using the Unicode APIs. When using long path names, prefix the path with the characters \\\\?\ and use the Unicode versions of the C Runtime functions.  
  
## See Also  
 [Global Constants](../vs140/Global-Constants.md)