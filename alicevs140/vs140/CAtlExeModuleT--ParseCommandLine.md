---
title: "CAtlExeModuleT::ParseCommandLine"
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
ms.assetid: 833dcad7-b888-439b-a3e2-9d2efe2c720a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlExeModuleT::ParseCommandLine
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
 The command line passed to the application.  
  
 `pnRetCode`  
 The HRESULT corresponding to the registration (if it took place).  
  
## Return Value  
 Return true if the application should continue to run, otherwise false.  
  
## Remarks  
 This method is called from [CAtlExeModuleT::WinMain](../vs140/CAtlExeModuleT--WinMain.md) and can be overridden to handle command-line switches. The default implementation checks for **/RegServer** and **/UnRegServer** command-line arguments and performs registration or unregistration.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlExeModuleT Class](../vs140/CAtlExeModuleT-Class.md)