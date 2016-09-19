---
title: "AtlHresultFromLastError"
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
ms.assetid: 74530d7d-3c91-484c-acf3-aff755715d66
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlHresultFromLastError
Returns the calling thread's last-error code value in the form of an HRESULT.  
  
## Syntax  
  
```  
  
HRESULT AtlHresultFromLastError( );  
  
```  
  
## Remarks  
 `AtlHresultFromLastError` calls `GetLastError` to obtain the last error and returns the error after converting it to an HRESULT using the **HRESULT_FROM_WIN32** macro.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [Debugging and Error Reporting Global Functions](../vs140/Debugging-and-Error-Reporting-Global-Functions.md)   
 [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360)   
 [HRESULT_FROM_WIN32](http://msdn.microsoft.com/library/windows/desktop/ms680746)   
 [AtlHresultFromWin32](../vs140/AtlHresultFromWin32.md)