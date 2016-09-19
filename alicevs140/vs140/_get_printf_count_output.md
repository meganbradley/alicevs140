---
title: "_get_printf_count_output"
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
apiname: 
  - _get_printf_count_output
apilocation: 
  - msvcr90.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 850f9f33-8319-433e-98d8-6a694200d994
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _get_printf_count_output
Indicates whether [printf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)-family functions support the `%n` format.  
  
## Syntax  
  
```  
int _get_printf_count_output();  
```  
  
## Return Value  
 Non-zero if `%n` is supported, 0 if `%n` is not supported.  
  
## Remarks  
 If `%n` is not supported (the default), encountering `%n` in the format string of any of the `printf` functions will invoke the invalid parameter handler as described in [Parameter Validation](../vs140/Parameter-Validation.md). If `%n` support is enabled (see [_set_printf_count_output](../vs140/_set_printf_count_output.md)) then `%n` will behave as described in [printf Type Field Characters](../vs140/printf-Type-Field-Characters.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_get_printf_count_output`|<stdio.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [_set_printf_count_output](../vs140/_set_printf_count_output.md).  
  
## NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).