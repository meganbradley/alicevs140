---
title: "SafeSubtract"
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
ms.topic: language-reference
ms.assetid: c2712ddc-173f-46a1-b09c-e7ebbd9e68b2
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SafeSubtract
Subtracts two numbers in a way that protects against overflow.  
  
## Syntax  
  
```  
template<typename T, typename U>  
inline bool SafeSubtract (  
   T t,  
   U u,  
   T& result  
) throw ();  
```  
  
#### Parameters  
 [in] `t`  
 The first number in the subtraction. This must be of type T.  
  
 [in] `u`  
 The number to subtract from `t`. This must be of type U.  
  
 [out] `result`  
 The parameter where `SafeSubtract` stores the result.  
  
## Return Value  
 `true` if no error occurs; `false` if an error occurs.  
  
## Remarks  
 This method is part of [The SafeInt Library](../vs140/SafeInt-Library.md) and is designed for a single subtraction operation without creating an instance of the [SafeInt Class](../vs140/SafeInt-Class.md).  
  
> [!NOTE]
>  This method should only be used when a single mathematical operation must be protected. If there are multiple operations, you should use the `SafeInt` class instead of calling the individual stand-alone functions.  
  
 For more information about the template types T and U, see [SafeInt Functions](../vs140/SafeInt-Functions.md).  
  
## Requirements  
 **Header:** safeint.h  
  
 **Namespace:** Microsoft::Utilities  
  
## See Also  
 [SafeInt Functions](../vs140/SafeInt-Functions.md)   
 [The SafeInt Library](../vs140/SafeInt-Library.md)   
 [SafeInt Class](../vs140/SafeInt-Class.md)   
 [SafeAdd](../vs140/SafeAdd.md)