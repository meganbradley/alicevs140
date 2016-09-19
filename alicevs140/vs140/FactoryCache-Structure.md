---
title: "FactoryCache Structure"
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
ms.assetid: 624544e6-0989-47f6-a3e9-edb60e1ee6d4
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FactoryCache Structure
Supports the [!INCLUDE[cppwrl](../vs140/includes/cppwrl_md.md)] infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
struct FactoryCache;  
```  
  
## Remarks  
 Contains the location of a class factory and a value that identifies a registered wrt or COM class object.  
  
## Members  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[FactoryCache::cookie Data Member](../vs140/FactoryCache--cookie-Data-Member.md)|Contains a value that identifies a registered [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] or COM class object, and is later used to unregister the object.|  
|[FactoryCache::factory Data Member](../vs140/FactoryCache--factory-Data-Member.md)|Points to a [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] or COM class factory.|  
  
## Inheritance Hierarchy  
 `FactoryCache`  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)