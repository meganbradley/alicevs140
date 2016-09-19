---
title: "OBJECT_ENTRY_NON_CREATEABLE_EX_AUTO"
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
ms.assetid: abdc093c-6502-42de-8419-b7ebf45299d1
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OBJECT_ENTRY_NON_CREATEABLE_EX_AUTO
Allows you to specify that the object should be registered and initialized, but it should not be externally creatable via `CoCreateInstance`.  
  
## Syntax  
  
```  
  
      OBJECT_ENTRY_NON_CREATEABLE_EX_AUTO(   
   clsid,   
   class    
)  
```  
  
#### Parameters  
 `clsid`  
 [in] The CLSID of a COM class implemented by the C++ class named `class`.  
  
 `class`  
 [in] The name of the C++ class implementing the COM class represented by `clsid`.  
  
## Remarks  
 Object entry macros are placed at global scope in the project to provide support for the registration, initialization, and creation of a class.  
  
 `OBJECT_ENTRY_NON_CREATEABLE_EX_AUTO` allows you to specify that an object should be registered and initialized (see [OBJECT_ENTRY_AUTO](../vs140/OBJECT_ENTRY_AUTO.md) for more information), but it should not be creatable via `CoCreateInstance`.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Object Map Macros](../vs140/Object-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [OBJECT_ENTRY_AUTO](../vs140/OBJECT_ENTRY_AUTO.md)