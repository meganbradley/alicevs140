---
title: "Constant and Global Variable Mappings"
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
ms.assetid: 3af4fd3e-9ed5-4ed9-96fd-7031e5126fd1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Constant and Global Variable Mappings
These generic-text constant, global variable, and standard-type mappings are defined in TCHAR.H and depend on whether the constant `_UNICODE` or `_MBCS` has been defined in your program.  
  
### Generic-Text Constant and Global Variable Mappings  
  
|Generic-text - object name|SBCS (_UNICODE, _MBCS not defined)|_MBCS defined|_UNICODE defined|  
|----------------------------------|--------------------------------------------|--------------------|-----------------------|  
|`_TEOF`|`EOF`|`EOF`|`WEOF`|  
|`_tenviron`|`_environ`|`_environ`|`_wenviron`|  
|`_tpgmptr`|`_pgmptr`|`_pgmptr`|`_wpgmptr`|  
  
## See Also  
 [Generic-Text Mappings](../vs140/Generic-Text-Mappings.md)   
 [Data Type Mappings](../vs140/Data-Type-Mappings.md)   
 [Routine Mappings](../vs140/Routine-Mappings.md)   
 [A Sample Generic-Text Program](../vs140/A-Sample-Generic-Text-Program.md)   
 [Using Generic-Text Mappings](../vs140/Using-Generic-Text-Mappings.md)