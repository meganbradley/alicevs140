---
title: "AfxDebugBreak (MFC)"
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
ms.assetid: c4cd79b9-9327-4db5-a9d6-c4004a92aa30
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxDebugBreak (MFC)
Call this function to cause a break (at the location of the call to `AfxDebugBreak`) in the execution of the debug version of your MFC application.  
  
## Syntax  
  
```  
  
void AfxDebugBreak( );  
  
```  
  
## Remarks  
 `AfxDebugBreak` has no effect in release versions of an MFC application and should be removed. This function should only be used in MFC applications. Use the Win32 API version, **DebugBreak**, to cause a break in non-MFC applications.  
  
## Requirements  
 **Header:** afxver_.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)