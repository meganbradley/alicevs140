---
title: "fixed Statement (C# Reference)"
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
ms.assetid: 7ea6db08-ad49-4a7a-b934-d8c4acad1c3a
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fixed Statement (C# Reference)
The `fixed` statement prevents the garbage collector from relocating a movable variable. The `fixed` statement is only permitted in an [unsafe](../vs140/unsafe--C#-Reference-.md) context. `Fixed` can also be used to create [fixed size buffers](../Topic/Fixed%20Size%20Buffers%20\(C%23%20Programming%20Guide\).md).  
  
 The `fixed` statement sets a pointer to a managed variable and "pins" that variable during the execution of the statement. Without `fixed`, pointers to movable managed variables would be of little use since garbage collection could relocate the variables unpredictably. The C# compiler only lets you assign a pointer to a managed variable in a `fixed` statement.  
  
 [!CODE [csrefKeywordsFixedLock#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsFixedLock#1)]  
  
 You can initialize a pointer by using an array, a string, a fixed-size buffer, or the address of a variable. The following example illustrates the use of variable addresses, arrays, and strings. For more information about fixed-size buffers, see [Fixed Size Buffers (C# Programming Guide)](../Topic/Fixed%20Size%20Buffers%20\(C%23%20Programming%20Guide\).md).  
  
 [!CODE [csrefKeywordsFixedLock#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsFixedLock#2)]  
  
 You can initialize multiple pointers, as long as they are all of the same type.  
  
```  
fixed (byte* ps = srcarray, pd = dstarray) {...}  
```  
  
 To initialize pointers of different types, simply nest `fixed` statements, as shown in the following example.  
  
 [!CODE [csrefKeywordsFixedLock#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsFixedLock#3)]  
  
 After the code in the statement is executed, any pinned variables are unpinned and subject to garbage collection. Therefore, do not point to those variables outside the `fixed` statement.  
  
> [!NOTE]
>  Pointers initialized in fixed statements cannot be modified.  
  
 In unsafe mode, you can allocate memory on the stack, where it is not subject to garbage collection and therefore does not need to be pinned. For more information, see [stackalloc](../vs140/stackalloc--C#-Reference-.md).  
  
## Example  
 [!CODE [csrefKeywordsFixedLock#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsFixedLock#4)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [unsafe](../vs140/unsafe--C#-Reference-.md)   
 [Fixed Size Buffers (C#)](../Topic/Fixed%20Size%20Buffers%20\(C%23%20Programming%20Guide\).md)