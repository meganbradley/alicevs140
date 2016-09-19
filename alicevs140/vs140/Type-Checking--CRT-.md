---
title: "Type Checking (CRT)"
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
ms.assetid: 1ba7590b-d1c0-4636-b6a0-e231395abdad
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type Checking (CRT)
The compiler performs limited type checking on functions that can take a variable number of arguments, as follows:  
  
|Function call|Type-checked arguments|  
|-------------------|-----------------------------|  
|`_cprintf_s`, `_cscanf_s`, `printf_s`, `scanf_s`|First argument (format string)|  
|`fprintf_s`, `fscanf_s`, `sprintf_s`, `sscanf_s`|First two arguments (file or buffer and format string)|  
|`_snprintf_s`|First three arguments (file or buffer, count, and format string)|  
|`_open`|First two arguments (path and `_open` flag)|  
|`_sopen_s`|First three arguments (path, `_open` flag, and sharing mode)|  
|`_execl`, `_execle`, `_execlp`, `_execlpe`|First two arguments (path and first argument pointer)|  
|`_spawnl`, `_spawnle`, `_spawnlp`, `_spawnlpe`|First three arguments (mode flag, path, and first argument pointer)|  
  
 The compiler performs the same limited type checking on the wide-character counterparts of these functions.  
  
## See Also  
 [CRT Library Features](../vs140/CRT-Library-Features.md)