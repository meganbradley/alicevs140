---
title: "__alignof Operator"
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
ms.assetid: acb1eed7-6398-40bd-b0c5-684ceb64afbc
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __alignof Operator
C++11 introduces the `alignof` operator that returns the alignment, in bytes, of the specified type. For maximum portability, you should use the alignof operator instead of the Microsoft-specific __alignof operator.  
  
 **Microsoft Specific**  
  
 Returns a value of type **size_t** that is the alignment requirement of the type.  
  
## Syntax  
  
```  
  
      __alignof(   
   type    
)  
```  
  
## Remarks  
 For example:  
  
|Expression|Value|  
|----------------|-----------|  
|**__alignof( char )**|1|  
|**__alignof( short )**|2|  
|**__alignof( int )**|4|  
|**__alignof( \__int64 )**|8|  
|**__alignof( float )**|4|  
|**__alignof( double )**|8|  
|**__alignof( char\* )**|4|  
  
 The `__alignof` value is the same as the value for `sizeof` for basic types. Consider, however, this example:  
  
```  
typedef struct { int a; double b; } S;  
// __alignof(S) == 8  
```  
  
 In this case, the `__alignof` value is the alignment requirement of the largest element in the structure.  
  
 Similarly, for  
  
```  
typedef __declspec(align(32)) struct { int a; } S;  
```  
  
 `__alignof(S)` is equal to `32`.  
  
 One use for `__alignof` would be as a parameter to one of your own memory-allocation routines. For example, given the following defined structure `S`, you could call a memory-allocation routine named `aligned_malloc` to allocate memory on a particular alignment boundary.  
  
```  
typedef __declspec(align(32)) struct { int a; double b; } S;  
int n = 50; // array size  
S* p = (S*)aligned_malloc(n * sizeof(S), __alignof(S));  
```  
  
 For more information on modifying alignment, see:  
  
-   [pack](../vs140/pack.md)  
  
-   [align](../vs140/align--C---.md)  
  
-   [__unaligned](../vs140/__unaligned.md)  
  
-   [/Zp (Struct Member Alignment)](../Topic/-Zp%20\(Struct%20Member%20Alignment\).md)  
  
-   [Structure Alignment Examples](../vs140/Examples-of-Structure-Alignment.md) (x64 specific)  
  
 For more information on differences in alignment in code for x86 and x64, see:  
  
-   [Conflicts with the x86 Compiler](../vs140/Conflicts-with-the-x86-Compiler.md)  
  
## END Microsoft Specific  
  
## See Also  
 [Expressions with Unary Operators](../vs140/Expressions-with-Unary-Operators.md)   
 [Keywords](../vs140/Keywords--C---.md)