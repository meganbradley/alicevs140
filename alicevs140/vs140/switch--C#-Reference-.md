---
title: "switch (C# Reference)"
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
ms.assetid: 44bae8b8-8841-4d85-826b-8a94277daecb
caps.latest.revision: 49
translation.priority.ht: 
  - de-de
  - ja-jp
---
# switch (C# Reference)
The `switch` statement is a control statement that selects a *switch section* to execute from a list of candidates.  
  
 A `switch` statement includes one or more switch sections. Each switch section contains one or more *case labels* followed by one or more statements. The following example shows a simple `switch` statement that has three switch sections. Each switch section has one case label, such as `case 1`, and two statements.  
  
 [!CODE [csrefKeywordsSelection#7](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#7)]  
  
## Remarks  
 Each case label specifies a constant value. The switch statement transfers control to the switch section whose case label matches the value of the *switch expression* (`caseSwitch` in the example). If no case label contains a matching value, control is transferred to the `default` section, if there is one. If there is no `default` section, no action is taken and control is transferred outside the `switch` statement. In the previous example, the statements in the first switch section are executed because `case 1` matches the value of `caseSwitch`.  
  
 A `switch` statement can include any number of switch sections, and each section can have one or more case labels (as shown in the string case labels example below). However, no two case labels may contain the same constant value.  
  
 Execution of the statement list in the selected switch section begins with the first statement and proceeds through the statement list, typically until a jump statement, such as a `break`, `goto case`, `return`, or `throw`, is reached. At that point, control is transferred outside the `switch` statement or to another case label.  
  
 Unlike C++, C# does not allow execution to continue from one switch section to the next. The following code causes an error.  
  
```c#  
switch (caseSwitch)  
{  
    // The following switch section causes an error.  
    case 1:  
        Console.WriteLine("Case 1...");  
        // Add a break or other jump statement here.  
    case 2:  
        Console.WriteLine("... and/or Case 2");  
        break;  
}  
```  
  
 C# requires the end of switch sections, including the final one, to be unreachable.  That is, unlike some other languages, your code may not fall through into the next switch section.  Although this requirement is usually met by using a `break` statement, the following case is also valid, because it ensures that the end of the statement list cannot be reached.  
  
```c#  
case 4:  
    while (true)  
        Console.WriteLine("Endless looping. . . .");  
```  
  
## Example  
 The following example illustrates the requirements and capabilities of a `switch` statement.  
  
 [!CODE [csrefKeywordsSelection#9](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#9)]  
  
## Example  
 In the final example, the string variable, `str`, and string case labels control the flow of execution.  
  
 [!CODE [csrefKeywordsSelection#8](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#8)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [switch Statement (C++)](../vs140/switch-Statement--C---.md)   
 [if-else](../vs140/if-else--C#-Reference-.md)