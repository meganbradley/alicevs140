---
title: "__p__commode"
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
ms.topic: article
apiname: 
  - __p__commode
apilocation: 
  - msvcr110.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - api-ms-win-crt-stdio-l1-1-0.dll
apitype: DLLExport
ms.assetid: 4380acb8-e3e4-409c-a60f-6205ac5189ce
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __p__commode
Points to the `_commode` global variable, which specifies the default *file commit mode* for file I/O operations.  
  
## Syntax  
  
```cpp  
int * __p__commode(  
   );  
```  
  
## Return Value  
 Pointer to the `_commode` global variable.  
  
## Remarks  
 The `__p__commode` function is for internal use only, and should not be called from user code.  
  
 File commit mode specifies when critical data is written to disk. For more information, see [fflush](../vs140/fflush.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|__p\__commode|internal.h|