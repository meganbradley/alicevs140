---
title: "Type and Variable Sizes in Inline Assembly"
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
ms.assetid: b62c2f2b-a7ad-4145-bae4-d890db86d348
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type and Variable Sizes in Inline Assembly
**Microsoft Specific**  
  
 The **LENGTH**, **SIZE**, and **TYPE** operators have a limited meaning in inline assembly. They cannot be used at all with the `DUP` operator (because you cannot define data with MASM directives or operators). But you can use them to find the size of C or C++ variables or types:  
  
-   The **LENGTH** operator can return the number of elements in an array. It returns the value 1 for non-array variables.  
  
-   The **SIZE** operator can return the size of a C or C++ variable. A variable's size is the product of its **LENGTH** and **TYPE**.  
  
-   The **TYPE** operator can return the size of a C or C++ type or variable. If the variable is an array, **TYPE** returns the size of a single element of the array.  
  
 For example, if your program has an 8-element `int` array,  
  
```  
int arr[8];  
```  
  
 the following C and assembly expressions yield the size of `arr` and its elements.  
  
|__asm|C|Size|  
|-------------|-------|----------|  
|**LENGTH** arr|`sizeof`(arr)/`sizeof`(arr[0])|8|  
|**SIZE** arr|`sizeof`(arr)|32|  
|**TYPE** arr|`sizeof`(arr[0])|4|  
  
 **END Microsoft Specific**  
  
## See Also  
 [Using Assembly Language in __asm Blocks](../vs140/Using-Assembly-Language-in-__asm-Blocks.md)