---
title: "CAtlExeModuleT::InitializeCom"
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
ms.assetid: 9efc5ce5-201d-4573-a2b7-9d8ed5071b26
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlExeModuleT::InitializeCom
Initializes COM.  
  
## Syntax  
  
```  
  
static HRESULT InitializeCom( ) throw( );  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method is called from the constructor and can be overridden to initialize COM in a manner different from the default implementation. The default implementation either calls **CoInitializeEx(NULL, COINIT_MULTITHREADED)** or **CoInitialize(NULL)** depending on the project configuration.  
  
 Overriding this method normally requires overriding [CAtlExeModuleT::UninitializeCom](../vs140/CAtlExeModuleT--UninitializeCom.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlExeModuleT Class](../vs140/CAtlExeModuleT-Class.md)   
 [CoInitialize](http://msdn.microsoft.com/library/windows/desktop/ms678543)   
 [CoInitializeEx](http://msdn.microsoft.com/library/windows/desktop/ms695279)