---
title: "CAtlExeModuleT::m_dwPause"
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
ms.assetid: 143af4d5-d80e-4a7a-8e73-871d6a5f6e92
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlExeModuleT::m_dwPause
A pause value used to ensure all objects are gone before shutdown.  
  
## Syntax  
  
```  
  
DWORD m_dwPause;  
  
```  
  
## Remarks  
 Change this value after calling [CAtlExeModuleT::InitializeCom](../vs140/CAtlExeModuleT--InitializeCom.md) to set the number of milliseconds used as the pause value for shutting down the server. The default value is 1000 milliseconds.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlExeModuleT Class](../vs140/CAtlExeModuleT-Class.md)