---
title: "AtlHresultFromWin32"
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
ms.assetid: 63add2dd-274c-4e72-a98c-040b93413a2f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlHresultFromWin32
Converts a Win32 error code into an HRESULT.  
  
## Syntax  
  
```  
  
      AtlHresultFromWin32{  
   DWORD error  
};  
```  
  
#### Parameters  
 *error*  
 The error value to convert.  
  
## Remarks  
 Converts a Win32 error code into an HRESULT, using the macro **HRESULT_FROM_WIN32**.  
  
> [!NOTE]
>  Instead of using **HRESULT_FROM_WIN32(GetLastError())**, use the function [AtlHresultFromLastError](../vs140/AtlHresultFromLastError.md).  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [Debugging and Error Reporting Global Functions](../vs140/Debugging-and-Error-Reporting-Global-Functions.md)   
 [HRESULT_FROM_WIN32](http://msdn.microsoft.com/library/windows/desktop/ms680746)   
 [AtlHresultFromLastError](../vs140/AtlHresultFromLastError.md)