---
title: "MakeAndInitialize Function"
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
ms.assetid: 71ceeb12-d2a2-4317-b010-3dcde1b39467
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MakeAndInitialize Function
Initializes the specified [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] class. Use this function to instantiate a component that is defined in the same module.  
  
## Syntax  
  
```cpp  
template <typename T, typename I,   
typename TArg1,   
typename TArg2,   
typename TArg3,   
typename TArg4,   
typename TArg5,   
typename TArg6,   
typename TArg7,   
typename TArg8,   
typename TArg9> HRESULT MakeAndInitialize(_Outptr_result_nullonfailure_ I** ppvObject, TArg1 &&arg1, TArg2 &&arg2, TArg3 &&arg3, TArg4 &&arg4, TArg5 &&arg5, TArg6 &&arg6, TArg7 &&arg7, TArg8 &&arg8, TArg9 &&arg9) throw()  
```  
  
#### Parameters  
 `T`  
 A user-specified class that inherits from `WRL::RuntimeClass`.  
  
 `TArg1`  
 Type of argument 1 that is passed to the specified runtime class.  
  
 `TArg2`  
 Type of argument 2 that is passed to the specified runtime class.  
  
 `TArg3`  
 Type of argument 3 that is passed to the specified runtime class.  
  
 `TArg4`  
 Type of argument 4 that is passed to the specified runtime class.  
  
 `TArg5`  
 Type of argument 5 that is passed to the specified runtime class.  
  
 `TArg6`  
 Type of argument 6 that is passed to the specified runtime class.  
  
 `TArg7`  
 Type of argument 7 that is passed to the specified runtime class.  
  
 `TArg8`  
 Type of argument 8 that is passed to the specified runtime class.  
  
 `TArg9`  
 Type of argument 9 that is passed to the specified runtime class.  
  
 `arg1`  
 Argument 1 that is passed to the specified runtime class.  
  
 `arg2`  
 Argument 2 that is passed to the specified runtime class.  
  
 `arg3`  
 Argument 3 that is passed to the specified runtime class.  
  
 `arg4`  
 Argument 4 that is passed to the specified runtime class.  
  
 `arg5`  
 Argument 5 that is passed to the specified runtime class.  
  
 `arg6`  
 Argument 6 that is passed to the specified runtime class.  
  
 `arg7`  
 Argument 7 that is passed to the specified runtime class.  
  
 `arg8`  
 Argument 8 that is passed to the specified runtime class.  
  
 `arg9`  
 Argument 9 that is passed to the specified runtime class.  
  
## Return Value  
 An `HRESULT` value.  
  
## Remarks  
 See [How to: Instantiate WRL Components Directly](../vs140/How-to--Instantiate-WRL-Components-Directly.md) to learn the differences between this function and [Microsoft::WRL::Make](../vs140/Make-Function.md), and for an example.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)