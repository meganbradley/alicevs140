---
title: "InspectableClass Macro"
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
ms.assetid: ff390b26-58cc-424f-87ac-1fe3cc692b59
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# InspectableClass Macro
Sets the runtime class name and trust level.  
  
## Syntax  
  
```cpp  
  
InspectableClass(  
   runtimeClassName,   
   trustLevel)  
```  
  
#### Parameters  
 `runtimeClassName`  
 The full textual name of the runtime class.  
  
 `trustLevel`  
 One of the [TrustLevel](http://msdn.microsoft.com/library/br224625.aspx) enumerated values.  
  
## Remarks  
 The `InspectableClass` macro can be used only with [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] types.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [RuntimeClass Class](../vs140/RuntimeClass-Class.md)