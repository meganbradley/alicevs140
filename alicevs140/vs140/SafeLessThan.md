---
title: "SafeLessThan"
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
ms.assetid: 9d85bc0d-8d94-4d59-9b72-ef3c63a120a0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SafeLessThan
Determines whether one number is less than another.  
  
## Syntax  
  
```  
template<typename T, typename U>  
inline bool SafeLessThan (  
   const T t,  
   const U u  
) throw ();  
```  
  
#### Parameters  
 [in] `t`  
 The first number. This must be of type T.  
  
 [in] `u`  
 The second numer. This must be of type U.  
  
## Return Value  
 `true` if `t` is less than `u`; otherwise `false`.  
  
## Remarks  
 This method enhances the standard comparison operator because `SafeLessThan` enables you to compare two different types of number.  
  
 This method is part of [The SafeInt Library](../vs140/SafeInt-Library.md) and is designed for a single comparison operation without creating an instance of the [SafeInt Class](../vs140/SafeInt-Class.md).  
  
> [!NOTE]
>  This method should only be used when a single mathematical operation must be protected. If there are multiple operations, you should use the `SafeInt` class rather than calling the individual stand-alone functions.  
  
 For more information about the template types T and U, see [SafeInt Functions](../vs140/SafeInt-Functions.md).  
  
## Requirements  
 **Header:** safeint.h  
  
 **Namespace:** Microsoft::Utilities  
  
## See Also  
 [SafeInt Functions](../vs140/SafeInt-Functions.md)   
 [The SafeInt Library](../vs140/SafeInt-Library.md)   
 [SafeInt Class](../vs140/SafeInt-Class.md)   
 [SafeLessThanEquals](../vs140/SafeLessThanEquals.md)   
 [SafeGreaterThan](../vs140/SafeGreaterThan.md)   
 [SafeGreaterThanEquals](../vs140/SafeGreaterThanEquals.md)