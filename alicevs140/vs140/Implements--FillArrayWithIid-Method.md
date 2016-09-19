---
title: "Implements::FillArrayWithIid Method"
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
ms.assetid: b2e62e3f-0ab9-4c70-aad7-856268544f44
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Implements::FillArrayWithIid Method
Inserts the interface ID specified by the current zeroth template parameter into the specified array element.  
  
## Syntax  
  
```  
__forceinline static void FillArrayWithIid(  
   unsigned long &index,  
   _In_ IID* iids  
);  
```  
  
#### Parameters  
 `index`  
 A zero-based index that indicates the starting array element for this operation. When this operation completes, `index` is incremented by 1.  
  
 `iids`  
 An array of type IID.  
  
## Remarks  
 Internal helper function.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Implements Structure](../vs140/Implements-Structure.md)