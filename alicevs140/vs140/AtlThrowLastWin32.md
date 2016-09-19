---
title: "AtlThrowLastWin32"
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
ms.assetid: 8bce8e56-c7cd-4ebb-8c62-80ebc63a3d07
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlThrowLastWin32
Call this function to signal an error based on the result of the Windows function `GetLastError`.  
  
## Syntax  
  
```  
  
inline void AtlThrowLastWin32( );  
  
```  
  
## Remarks  
 This function traces the result of `GetLastError` to the debugger.  
  
 If **_ATL_NO_EXCEPTIONS** is not defined in an MFC project, this function throws a [CMemoryException](../vs140/CMemoryException-Class.md) or a [COleException](../vs140/COleException-Class.md) based on the value returned by `GetLastError`.  
  
 If **_ATL_NO_EXCEPTIONS** is not defined in an ATL project, the function throws a [CAtlException](../vs140/CAtlException-Class.md).  
  
 If **_ATL_NO_EXCEPTIONS** is defined, the function causes an assertion failure instead of throwing an exception.  
  
## Requirements  
 **Header:** atldef.h  
  
## See Also  
 [Debugging and Error Reporting Global Functions](../vs140/Debugging-and-Error-Reporting-Global-Functions.md)   
 [ATLTRACE2](../vs140/ATLTRACE2.md)   
 [AtlThrow](../vs140/AtlThrow.md)   
 [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360)