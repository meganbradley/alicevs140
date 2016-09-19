---
title: "FactoryCache::cookie Data Member"
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
ms.assetid: b1bc79af-a896-4e3b-8afa-64733022eddf
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FactoryCache::cookie Data Member
Supports the [!INCLUDE[cppwrl](../vs140/includes/cppwrl_md.md)] infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
union {   
   WINRT_REGISTRATION_COOKIE winrt;  
   DWORD com;   
} cookie;  
```  
  
## Remarks  
 Contains a value that identifies a registered [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] or COM class object, and is later used to unregister the object.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [FactoryCache Structure](../vs140/FactoryCache-Structure.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)