---
title: "Yield Statement (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f33126c5-d7c4-43e2-8e36-4ae3f0703d97
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Yield Statement (Visual Basic)
Sends the next element of a collection to a `For Each...Next` statement.  
  
## Syntax  
  
```  
Yield expression  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Term|Definition|  
|`expression`|Required. An expression that is implicitly convertible to the type of the iterator function or `Get` accessor that contains the `Yield` statement.|  
  
## Remarks  
 The `Yield` statement returns one element of a collection at a time. The `Yield` statement is included in an iterator function or `Get` accessor, which perform custom iterations over a collection.  
  
 You consume an iterator function by using a [For Each...Next Statement (Visual Basic)](../Topic/For%20Each...Next%20Statement%20\(Visual%20Basic\).md) or a LINQ query. Each iteration of the `For Each` loop calls the iterator function. When a `Yield` statement is reached in the iterator function, `expression` is returned, and the current location in code is retained. Execution is restarted from that location the next time that the iterator function is called.  
  
 An implicit conversion must exist from the type of `expression` in the `Yield` statement to the return type of the iterator.  
  
 You can use an `Exit Function` or `Return` statement to end the iteration.  
  
 "Yield" is not a reserved word and has special meaning only when it is used in an `Iterator` function or `Get` accessor.  
  
 For more information about iterator functions and `Get` accessors, see [Iterators (C# and Visual Basic)](../vs140/Iterators--C#-and-Visual-Basic-.md).  
  
## Iterator Functions and Get Accessors  
 The declaration of an iterator function or `Get` accessor must meet the following requirements:  
  
-   It must include an [Iterator](../Topic/Iterator%20\(Visual%20Basic\).md) modifier.  
  
-   The return type must be <xref:System.Collections.IEnumerable?qualifyHint=False>, <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False>, <xref:System.Collections.IEnumerator?qualifyHint=False>, or <xref:System.Collections.Generic.IEnumerator`1?qualifyHint=False>.  
  
-   It cannot have any `ByRef` parameters.  
  
 An iterator function cannot occur in an event, instance constructor, static constructor, or static destructor.  
  
 An iterator function can be an anonymous function. For more information, see [Iterators (C# and Visual Basic)](../vs140/Iterators--C#-and-Visual-Basic-.md).  
  
## Exception Handling  
 A `Yield` statement can be inside a `Try` block of a [Try...Catch...Finally Statement (Visual Basic)](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md). A `Try` block that has a `Yield` statement can have `Catch` blocks, and can have a `Finally` block.  
  
 A `Yield` statement cannot be inside a `Catch` block or a `Finally` block.  
  
 If the `For Each` body (outside of the iterator function) throws an exception, a `Catch` block in the iterator function is not executed, but a `Finally` block in the iterator function is executed. A `Catch` block inside an iterator function catches only exceptions that occur inside the iterator function.  
  
## Technical Implementation  
 The following code returns an `IEnumerable (Of String)` from an iterator function and then iterates through the elements of the `IEnumerable (Of String)`.  
  
```vb  
Dim elements As IEnumerable(Of String) = MyIteratorFunction()  
    …  
For Each element As String In elements  
Next  
```  
  
 The call to `MyIteratorFunction` doesn't execute the body of the function. Instead the call returns an `IEnumerable(Of String)` into the `elements` variable.  
  
 On an iteration of the `For Each` loop, the <xref:System.Collections.IEnumerator.MoveNext?qualifyHint=False> method is called for `elements`. This call executes the body of `MyIteratorFunction` until the next `Yield` statement is reached. The `Yield` statement returns an expression that determines not only the value of the `element` variable for consumption by the loop body but also the <xref:System.Collections.Generic.IEnumerator`1.Current?qualifyHint=False> property of elements, which is an `IEnumerable (Of String)`.  
  
 On each subsequent iteration of the `For Each` loop, the execution of the iterator body continues from where it left off, again stopping when it reaches a `Yield` statement. The `For Each` loop completes when the end of the iterator function or a `Return` or `Exit Function` statement is reached.  
  
## Example  
 The following example has a `Yield` statement that is inside a [For…Next](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md) loop. Each iteration of the [For Each](../Topic/For%20Each...Next%20Statement%20\(Visual%20Basic\).md) statement body in `Main` creates a call to the `Power` iterator function. Each call to the iterator function proceeds to the next execution of the `Yield` statement, which occurs during the next iteration of the `For…Next` loop.  
  
 The return type of the iterator method is <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False>, an iterator interface type. When the iterator method is called, it returns an enumerable object that contains the powers of a number.  
  
 [!CODE [VbVbalrStatements#98](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#98)]  
  
## Example  
 The following example demonstrates a `Get` accessor that is an iterator. The property declaration includes an `Iterator` modifier.  
  
 [!CODE [VbVbalrStatements#99](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#99)]  
  
 For additional examples, see [Iterators (C# and Visual Basic)](../vs140/Iterators--C#-and-Visual-Basic-.md).  
  
## Requirements  
 [!INCLUDE[vs_dev11_long](../vs140/includes/vs_dev11_long_md.md)]  
  
## See Also  
 [Iterators (C# and Visual Basic)](../vs140/Iterators--C#-and-Visual-Basic-.md)   
 [Statements (Visual Basic)](../vs140/Statements--Visual-Basic-.md)