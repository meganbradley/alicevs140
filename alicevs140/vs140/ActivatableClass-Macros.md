---
title: "ActivatableClass Macros"
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
ms.assetid: 9bd64709-ec2c-4678-8c96-ea5982622bdd
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ActivatableClass Macros
Populates an internal cache that contains a factory that can create an instance of the specified class.  
  
## Syntax  
  
```cpp  
ActivatableClass(  
   className  
);  
  
ActivatableClassWithFactory(  
   className,   
   factory  
);  
  
ActivatableClassWithFactoryEx(  
   className,   
   factory,   
   serverName  
);  
  
```  
  
#### Parameters  
 `className`  
 Name of the class to create.  
  
 `factory`  
 Factory that will create an instance of the specified class.  
  
 `serverName`  
 A name that specifies a subset of factories in the module.  
  
## Remarks  
 Do not use these macros with classic COM unless you use the `#undef` directive to ensure that the **__WRL_WINRT_STRICT\_\_** macro definition is removed.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Module Class](../vs140/Module-Class.md)