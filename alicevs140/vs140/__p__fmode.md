---
title: "__p__fmode"
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
  - __p__fmode
apilocation: 
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 1daa1394-81eb-43aa-a71b-4cc6acf3207b
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __p__fmode
Points to the `_fmode` global variable, which specifies the default *file translation mode* for file I/O operations.  
  
## Syntax  
  
```cpp  
int* __p__fmode(  
   );  
```  
  
## Return Value  
 Pointer to the `_fmode` global variable.  
  
## Remarks  
 The `__p__fmode` function is for internal use only, and should not be called from user code.  
  
 File translation mode specifies either `binary` or `text` translation for [_open](../Topic/_open,%20_wopen.md) and [_pipe](../vs140/_pipe.md) I/O operations. For more information, see [_fmode](../vs140/_fmode.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|__p\__fmode|stdlib.h|