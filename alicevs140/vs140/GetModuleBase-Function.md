---
title: "GetModuleBase Function"
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
ms.assetid: 123d3b14-2eaf-4e02-8dcd-b6567917c6a6
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetModuleBase Function
Retrieves a [ModuleBase](../vs140/ModuleBase-Class.md) pointer that allows for incrementing and decrementing the reference count of a [RuntimeClass](../vs140/RuntimeClass-Class.md) object.  
  
## Syntax  
  
```cpp  
inline Details::ModuleBase* GetModuleBase() throw()  
```  
  
## Return Value  
 A pointer to a `ModuleBase` object.  
  
## Remarks  
 This function is used internally to increment and decrement object reference counts.  
  
 You can use this function to control reference counts by calling [ModuleBase::IncrementObjectCount](../vs140/ModuleBase--IncrementObjectCount-Method.md) and [ModuleBase::DecrementObjectCount](../vs140/ModuleBase--DecrementObjectCount-Method.md).  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Microsoft::WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)