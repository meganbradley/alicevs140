---
title: "ChainInterfaces::FillArrayWithIid Method"
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
ms.assetid: f1ce699c-dfb6-40a9-9ea0-e6703d3cf971
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ChainInterfaces::FillArrayWithIid Method
Stores the interface ID defined by the `I0` template parameter into a specified location in a specified array of interface IDs.  
  
## Syntax  
  
```  
__forceinline static void FillArrayWithIid(  
   _Inout_ unsigned long &index,  
   _In_ IID* iids  
);  
```  
  
#### Parameters  
 `index`  
 Pointer to an index value into the `iids` array.  
  
 `iids`  
 An array of interface IDs.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ChainInterfaces Structure](../vs140/ChainInterfaces-Structure.md)