---
title: "FactoryCacheFlags Enumeration"
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
ms.assetid: 6f54258f-0144-4264-9608-414e5905f6fb
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FactoryCacheFlags Enumeration
Determines whether factory objects are cached.  
  
## Syntax  
  
```cpp  
enum FactoryCacheFlags;  
```  
  
## Remarks  
 By default, the factory caching policy is specified as the [ModuleType](../vs140/ModuleType-Enumeration.md) template parameter when you create a [Module](../vs140/Module-Class.md) object. To override this policy, specify a `FactoryCacheFlags` value when you create a factory object.  
  
|||  
|-|-|  
|`FactoryCacheDefault`|The caching policy of the `Module` object is used.|  
|`FactoryCacheEnabled`|Enables factory caching regardless of the `ModuleType` template parameter that is used to create a `Module` object.|  
|`FactoryCacheDisabled`|Disables factory caching regardless of the `ModuleType` template parameter that is used to create a `Module` object.|  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Microsoft::WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)