---
title: "CAtlServiceModuleT::ParseCommandLine"
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
ms.assetid: 504f0a64-4143-4d57-9562-d30381fe0d0e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::ParseCommandLine
Parses the command line and performs registration if necessary.  
  
## Syntax  
  
```  
  
      bool ParseCommandLine(  
   LPCTSTR lpCmdLine,  
   HRESULT* pnRetCode   
) throw( );  
```  
  
#### Parameters  
 `lpCmdLine`  
 The command line.  
  
 `pnRetCode`  
 The HRESULT corresponding to the registration (if it took place).  
  
## Return Value  
 Returns true on success, or false if the RGS file supplied in the command line could not be registered.  
  
## Remarks  
 Parses the command line and registers or unregisters the supplied RGS file if necessary. This method calls [CAtlExeModuleT::ParseCommandLine](../vs140/CAtlExeModuleT--ParseCommandLine.md) to check for **/RegServer** and **/UnregServer**. Adding the argument **-/Service** will register the service.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlServiceModuleT Class](../vs140/CAtlServiceModuleT-Class.md)   
 [CAtlExeModuleT::ParseCommandLine](../vs140/CAtlExeModuleT--ParseCommandLine.md)