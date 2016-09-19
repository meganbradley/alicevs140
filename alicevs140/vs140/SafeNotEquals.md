---
title: "SafeNotEquals"
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
ms.assetid: 032e45a8-4159-4b55-b7cc-ecd27f4e4788
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SafeNotEquals
Determines if two numbers are not equal.  
  
## Syntax  
  
```  
template<typename T, typename U>  
inline bool SafeNotEquals (  
   const T t,  
   const U u  
) throw ();  
```  
  
#### Parameters  
 [in] `t`  
 The first number to compare. This must be of type T.  
  
 [in] `u`  
 The second number to compare. This must be of type U.  
  
## Return Value  
 `true` if `t` and `u` are not equal; otherwise `false`.  
  
## Remarks  
 The method enhances `!=` because `SafeNotEquals` enables you to compare two different types of numbers.  
  
 This method is part of [The SafeInt Library](../vs140/SafeInt-Library.md) and is designed for a single comparison operation without creating an instance of the [SafeInt Class](../vs140/SafeInt-Class.md).  
  
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
 [SafeEquals](../vs140/SafeEquals.md)