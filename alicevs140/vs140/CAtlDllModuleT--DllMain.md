---
title: "CAtlDllModuleT::DllMain"
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
ms.assetid: 0defbd20-f8dc-4772-9b4d-1f272249510d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlDllModuleT::DllMain
The optional entry point into a dynamic-link library (DLL).  
  
## Syntax  
  
```  
  
      BOOL WINAPI DllMain(  
   DWORD dwReason,  
   LPVOID /*lpReserved*/  
) throw( );  
```  
  
#### Parameters  
 `dwReason`  
 If set to DLL_PROCESS_ATTACH, the DLL_THREAD_ATTACH and DLL_THREAD_DETACH notification calls are disabled.  
  
 *lpReserved*  
 Reserved.  
  
## Return Value  
 Always returns TRUE.  
  
## Remarks  
 Disabling the DLL_THREAD_ATTACH and DLL_THREAD_DETACH notification calls can be a useful optimization for multithreaded applications that have many DLLs, that frequently create and delete threads, and whose DLLs do not need these thread-level notifications of attachment/detachment.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlDllModuleT Class](../vs140/CAtlDllModuleT-Class.md)   
 [DisableThreadLibraryCalls](http://msdn.microsoft.com/library/windows/desktop/ms682579)   
 [DllMain](http://msdn.microsoft.com/library/windows/desktop/ms682583)