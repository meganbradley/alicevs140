---
title: "Implements::CastToUnknown Method"
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
ms.assetid: ca3324f7-4136-406b-8698-7389f4f3d3c7
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Implements::CastToUnknown Method
Gets a pointer to the underlying IUnknown interface.  
  
## Syntax  
  
```  
__forceinline IUnknown* CastToUnknown();  
```  
  
## Return Value  
 This operation always succeeds and returns the IUnknown pointer.  
  
## Remarks  
 Internal helper function.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Implements Structure](../vs140/Implements-Structure.md)