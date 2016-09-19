---
title: "Move Function"
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
ms.assetid: c9525426-97e8-4d8c-9877-b689d8a0dc67
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Move Function
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template<  
   class T  
>  
inline typename RemoveReference<T>::Type&& Move(  
   _Inout_ T&& arg  
);  
```  
  
#### Parameters  
 `T`  
 The type of the argument.  
  
 `arg`  
 An argument to move.  
  
## Return Value  
 Parameter `arg` after reference or rvalue-reference traits, if any, have been removed.  
  
## Remarks  
 Moves the specified argument from one location to another.  
  
 For more information, see the **Move Semantics** section of [Rvalue Reference Declarator: &&](../vs140/Rvalue-Reference-Declarator----.md).  
  
## Requirements  
 **Header:** internal.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)