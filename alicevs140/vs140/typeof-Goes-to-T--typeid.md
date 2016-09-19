---
title: "typeof Goes to T::typeid"
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
ms.topic: article
ms.assetid: 6a0d35a7-7a1a-4070-b187-cff37cfdc205
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# typeof Goes to T::typeid
The `typeof` operator used in Managed Extensions for C++ has been supplanted by the `typeid` keyword in [!INCLUDE[cpp_current_long](../vs140/includes/cpp_current_long_md.md)].  
  
 In Managed Extensions, the `__typeof()` operator returns the associated `Type*` object when passed the name of a managed type. For example:  
  
```  
// Creates and initializes a new Array instance.  
Array* myIntArray =   
   Array::CreateInstance( __typeof(Int32), 5 );  
```  
  
 In the new syntax, `__typeof` has been replaced by an additional form of `typeid` that returns a `Type^` when a managed type is specified.  
  
```  
// Creates and initializes a new Array instance.  
Array^ myIntArray =   
   Array::CreateInstance( Int32::typeid, 5 );  
```  
  
## See Also  
 [General Language Changes](../vs140/General-Language-Changes--C---CLI-.md)   
 [typeid](../Topic/typeid%20%20\(C++%20Component%20Extensions\).md)