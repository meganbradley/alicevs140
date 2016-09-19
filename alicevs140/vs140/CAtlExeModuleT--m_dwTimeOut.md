---
title: "CAtlExeModuleT::m_dwTimeOut"
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
ms.assetid: 14eb29a9-0cc1-4da1-8644-f2a97dce8bca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlExeModuleT::m_dwTimeOut
A time-out value used to delay the unloading of the module.  
  
## Syntax  
  
```  
  
DWORD m_dwTimeOut;  
  
```  
  
## Remarks  
 Change this value after calling [CAtlExeModuleT::InitializeCom](../vs140/CAtlExeModuleT--InitializeCom.md) to define the number of milliseconds used as the time-out value for shutting down the server. The default value is 5000 milliseconds. See the [CAtlExeModuleT Overview](../vs140/CAtlExeModuleT-Class.md) for more details.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlExeModuleT Class](../vs140/CAtlExeModuleT-Class.md)