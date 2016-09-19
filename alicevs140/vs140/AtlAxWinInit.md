---
title: "AtlAxWinInit"
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
ms.assetid: fe1b3bd1-3fc9-42e5-ba03-66cae7dd5b7e
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlAxWinInit
This function initializes ATL's control hosting code by registering the **"AtlAxWin80"** and **"AtlAxWinLic80"** window classes plus a couple of custom window messages.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
ATLAPI_(BOOL) AtlAxWinInit( );  
  
```  
  
## Return Value  
 Nonzero if the initialization of the control hosting code was successful; otherwise **FALSE**.  
  
## Remarks  
 This function must be called before using the [ATL control hosting API](../vs140/What-Is-the-ATL-Control-Hosting-API-.md). Following a call to this function, the **"AtlAxWin"** window class can be used in calls to [CreateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632679) or [CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more details on when to call this function, see [When Do I Need To Call AtlAxWinInit?](../vs140/When-Do-I-Need-to-Call-AtlAxWinInit-.md)  
  
## Requirements  
 **Header:** atlhost.h  
  
## See Also  
 [Composite Control Global Functions](../vs140/Composite-Control-Global-Functions.md)   
 [Composite Control Fundamentals](../vs140/ATL-Composite-Control-Fundamentals.md)   
 [AtlAxWinTerm](../vs140/AtlAxWinTerm.md)