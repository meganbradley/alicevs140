---
title: "CAtlExeModuleT::UninitializeCom"
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
ms.assetid: 5a07b3b5-8bb2-4e70-81ec-64a84e1b9be5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlExeModuleT::UninitializeCom
Uninitializes COM.  
  
## Syntax  
  
```  
  
static void UninitializeCom( ) throw( );  
  
```  
  
## Remarks  
 By default this method simply calls [CoUninitialize](http://msdn.microsoft.com/library/windows/desktop/ms688715) and is called from the destructor. Override this method if you override [CAtlExeModuleT::InitializeCom](../vs140/CAtlExeModuleT--InitializeCom.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlExeModuleT Class](../vs140/CAtlExeModuleT-Class.md)