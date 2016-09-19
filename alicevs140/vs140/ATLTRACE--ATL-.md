---
title: "ATLTRACE (ATL)"
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
ms.assetid: c796baa5-e2b9-4814-a27d-d800590b102e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLTRACE (ATL)
Reports warnings to an output device, such as the debugger window, according to the indicated flags and levels. Included for backward compatibility.  
  
## Syntax  
  
```  
  
      ATLTRACE(   
      exp   
      );  
ATLTRACE(  
   DWORD category,  
   UINT level,  
   LPCSTR lpszFormat,  
...  
);  
```  
  
#### Parameters  
 `exp`  
 [in] The string and variables to send to the Visual C++ output window or any application that traps these messages.  
  
 `category`  
 [in] Type of event or method on which to report. See the Remarks for a list of categories.  
  
 `level`  
 [in] The level of tracing to report. See the Remarks for details.  
  
 `lpszFormat`  
 [in] The formatted string to send to the dump device.  
  
## Remarks  
 See [ATLTRACE2](../vs140/ATLTRACE2.md) for a description of **ATLTRACE**. **ATLTRACE** and `ATLTRACE2` have the same behavior, **ATLTRACE** is included for backward compatibility.  
  
## Requirements  
 **Header:** atltrace.h  
  
## See Also  
 [Debugging and Error Reporting Macros](../vs140/Debugging-and-Error-Reporting-Macros.md)   
 [ATLTRACE2](../vs140/ATLTRACE2.md)