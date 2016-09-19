---
title: "How to: Obtain the Value of a Pointer Variable (C# Programming Guide)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 460a813a-4995-44c1-9de2-213b91dc7668
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Obtain the Value of a Pointer Variable (C# Programming Guide)
Use the pointer indirection operator to obtain the variable at the location pointed to by a pointer. The expression takes the following form, where `p` is a pointer type:  
  
```  
*p;  
```  
  
 You cannot use the unary indirection operator on an expression of any type other than the pointer type. Also, you cannot apply it to a [void](../vs140/void--C#-Reference-.md) pointer.  
  
 When you apply the indirection operator to a [null](../vs140/null--C#-Reference-.md) pointer, the result depends on the implementation.  
  
## Example  
 In the following example, a variable of the type `char` is accessed by using pointers of different types. Note that the address of `theChar` will vary from run to run, because the physical address allocated to a variable can change.  
  
 [!CODE [csProgGuidePointers#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#5)]  
  
 [!CODE [csProgGuidePointers#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#6)]  
  
 **Value of theChar = Z**   
**Address of theChar = 12F718**  
**Value of pChar = Z**   
**Value of pInt = 90**    
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Pointer Expressions](../vs140/Pointer-Expressions--C#-Programming-Guide-.md)   
 [Pointer types](../vs140/Pointer-types--C#-Programming-Guide-.md)   
 [Types](../vs140/Types--C#-Reference-.md)   
 [unsafe](../vs140/unsafe--C#-Reference-.md)   
 [fixed Statement](../vs140/fixed-Statement--C#-Reference-.md)   
 [stackalloc](../vs140/stackalloc--C#-Reference-.md)