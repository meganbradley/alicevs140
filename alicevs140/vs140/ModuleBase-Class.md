---
title: "ModuleBase Class"
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
ms.assetid: edce7591-6893-46f7-94a7-382827775548
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ModuleBase Class
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
class ModuleBase;  
```  
  
## Remarks  
 Represents the base class of the [Module](../vs140/Module-Class.md) classes.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[ModuleBase::ModuleBase Constructor](../vs140/ModuleBase--ModuleBase-Constructor.md)|Initializes an instance of the Module class.|  
|[ModuleBase::~ModuleBase Destructor](../vs140/ModuleBase--~ModuleBase-Destructor.md)|Deinitializes the current instance of the Module class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ModuleBase::DecrementObjectCount Method](../vs140/ModuleBase--DecrementObjectCount-Method.md)|When implemented, decrements the number of objects tracked by the module.|  
|[ModuleBase::IncrementObjectCount Method](../vs140/ModuleBase--IncrementObjectCount-Method.md)|When implemented, increments the number of objects tracked by the module.|  
  
## Inheritance Hierarchy  
 `ModuleBase`  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)