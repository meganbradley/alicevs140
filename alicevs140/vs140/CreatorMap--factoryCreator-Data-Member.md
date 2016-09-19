---
title: "CreatorMap::factoryCreator Data Member"
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
ms.assetid: c9aac363-8f38-4cfd-9605-1e6ac74c5097
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CreatorMap::factoryCreator Data Member
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
HRESULT (*factoryCreator)(  
   unsigned int* currentflags,  
   const CreatorMap* entry,  
   REFIID iidClassFactory,  
 IUnknown** factory);  
```  
  
## Parameters  
 `currentflags`  
 One of the [RuntimeClassType](../vs140/RuntimeClassType-Enumeration.md) enumerators.  
  
 `entry`  
 A CreatorMap.  
  
 `iidClassFactory`  
 The interface ID of a class factory.  
  
 `factory`  
 When the operation completes, the address of a class factory.  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that indicates the error.  
  
## Remarks  
 Creates a factory for the specified CreatorMap.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [CreatorMap Structure](../vs140/CreatorMap-Structure.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)