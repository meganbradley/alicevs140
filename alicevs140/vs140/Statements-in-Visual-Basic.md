---
title: "Statements in Visual Basic"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fcfdee1a-82b7-4846-98f7-9ca3f5160089
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Statements in Visual Basic
A statement in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] is a complete instruction. It can contain keywords, operators, variables, constants, and expressions. Each statement belongs to one of the following categories:  
  
-   **Declaration Statements**, which name a variable, constant, or procedure, and can also specify a data type.  
  
-   **Executable Statements**, which initiate actions. These statements can call a method or function, and they can loop or branch through blocks of code. Executable statements include **Assignment Statements**, which assign a value or expression to a variable or constant.  
  
 This topic describes each category. Also, this topic describes how to combine multiple statements on a single line and how to continue a statement over multiple lines.  
  
## Declaration Statements  
 You use declaration statements to name and define procedures, variables, properties, arrays, and constants. When you declare a programming element, you can also define its data type, access level, and scope. For more information, see [Declared Element Characteristics](../vs140/Declared-Element-Characteristics--Visual-Basic-.md).  
  
 The following example contains three declarations.  
  
 [!CODE [VbVbalrStatements#80](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#80)]  
  
 The first declaration is the `Sub` statement. Together with its matching `End Sub` statement, it declares a procedure named `applyFormat`. It also specifies that `applyFormat` is `Public`, which means that any code that can refer to it can call it.  
  
 The second declaration is the `Const` statement, which declares the constant `limit`, specifying the `Integer` data type and a value of 33.  
  
 The third declaration is the `Dim` statement, which declares the variable `thisWidget`. The data type is a specific object, namely an object created from the `Widget` class. You can declare a variable to be of any elementary data type or of any object type that is exposed in the application you are using.  
  
### Initial Values  
 When the code containing a declaration statement runs, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] reserves the memory required for the declared element. If the element holds a value, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] initializes it to the default value for its data type. For more information, see "Behavior" in [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md).  
  
 You can assign an initial value to a variable as part of its declaration, as the following example illustrates.  
  
 [!CODE [VbVbalrStatements#81](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#81)]  
  
 If a variable is an object variable, you can explicitly create an instance of its class when you declare it by using the [New (Visual Basic)](../vs140/New-Operator--Visual-Basic-.md) keyword, as the following example illustrates.  
  
 [!CODE [VbVbalrStatements#82](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#82)]  
  
 Note that the initial value you specify in a declaration statement is not assigned to a variable until execution reaches its declaration statement. Until that time, the variable contains the default value for its data type.  
  
## Executable Statements  
 An executable statement performs an action. It can call a procedure, branch to another place in the code, loop through several statements, or evaluate an expression. An assignment statement is a special case of an executable statement.  
  
 The following example uses an `If...Then...Else` control structure to run different blocks of code based on the value of a variable. Within each block of code, a `For...Next` loop runs a specified number of times.  
  
 [!CODE [VbVbalrStatements#83](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#83)]  
  
 The `If` statement in the preceding example checks the value of the parameter `clockwise`. If the value is `True`, it calls the `spinClockwise` method of `aWidget`. If the value is `False`, it calls the `spinCounterClockwise` method of `aWidget`. The `If...Then...Else` control structure ends with `End If`.  
  
 The `For...Next` loop within each block calls the appropriate method a number of times equal to the value of the `revolutions` parameter.  
  
## Assignment Statements  
 Assignment statements carry out assignment operations, which consist of taking the value on the right side of the assignment operator (`=`) and storing it in the element on the left, as in the following example.  
  
 [!CODE [VbVbalrStatements#73](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#73)]  
  
 In the preceding example, the assignment statement stores the literal value 42 in the variable `v`.  
  
### Eligible Programming Elements  
 The programming element on the left side of the assignment operator must be able to accept and store a value. This means it must be a variable or property that is not [ReadOnly (Visual Basic)](../vs140/ReadOnly--Visual-Basic-.md), or it must be an array element. In the context of an assignment statement, such an element is sometimes called an *lvalue*, for "left value."  
  
 The value on the right side of the assignment operator is generated by an expression, which can consist of any combination of literals, constants, variables, properties, array elements, other expressions, or function calls. The following example illustrates this.  
  
 [!CODE [VbVbalrStatements#74](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#74)]  
  
 The preceding example adds the value held in variable `y` to the value held in variable `z`, and then adds the value returned by the call to function `findResult`. The total value of this expression is then stored in variable `x`.  
  
### Data Types in Assignment Statements  
 In addition to numeric values, the assignment operator can also assign `String` values, as the following example illustrates.  
  
 [!CODE [VbVbalrStatements#75](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#75)]  
  
 You can also assign `Boolean` values, using either a `Boolean` literal or a `Boolean` expression, as the following example illustrates.  
  
 [!CODE [VbVbalrStatements#76](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#76)]  
  
 Similarly, you can assign appropriate values to programming elements of the `Char`, `Date`, or `Object` data type. You can also assign an object instance to an element declared to be of the class from which that instance is created.  
  
### Compound Assignment Statements  
 *Compound assignment statements* first perform an operation on an expression before assigning it to a programming element. The following example illustrates one of these operators, `+=`, which increments the value of the variable on the left side of the operator by the value of the expression on the right.  
  
 [!CODE [VbVbalrStatements#77](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#77)]  
  
 The preceding example adds 1 to the value of `n`, and then stores that new value in `n`. It is a shorthand equivalent of the following statement:  
  
 [!CODE [VbVbalrStatements#78](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#78)]  
  
 A variety of compound assignment operations can be performed using operators of this type. For a list of these operators and more information about them, see [Assignment Operators](../vs140/Assignment-Operators--Visual-Basic-.md).  
  
 The concatenation assignment operator (`&=`) is useful for adding a string to the end of already existing strings, as the following example illustrates.  
  
 [!CODE [VbVbalrStatements#79](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#79)]  
  
### Type Conversions in Assignment Statements  
 The value you assign to a variable, property, or array element must be of a data type appropriate to that destination element. In general, you should try to generate a value of the same data type as that of the destination element. However, some types can be converted to other types during assignment.  
  
 For information on converting between data types, see [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md). In brief, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] automatically converts a value of a given type to any other type to which it widens. A *widening conversion* is one in that always succeeds at run time and does not lose any data. For example, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] converts an `Integer` value to `Double` when appropriate, because `Integer` widens to `Double`. For more information, see [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md).  
  
 *Narrowing conversions* (those that are not widening) carry a risk of failure at run time, or of data loss. You can perform a narrowing conversion explicitly by using a type conversion function, or you can direct the compiler to perform all conversions implicitly by setting `Option Strict Off`. For more information, see [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md).  
  
## Putting Multiple Statements on One Line  
 You can have multiple statements on a single line separated by the colon (`:`) character. The following example illustrates this.  
  
 [!CODE [VbVbalrStatements#70](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#70)]  
  
 Though occasionally convenient, this form of syntax makes your code hard to read and maintain. Thus, it is recommended that you keep one statement to a line.  
  
## Continuing a Statement over Multiple Lines  
 A statement usually fits on one line, but when it is too long, you can continue it onto the next line using a line-continuation sequence, which consists of a space followed by an underscore character (`_`) followed by a carriage return. In the following example, the `MsgBox` executable statement is continued over two lines.  
  
 [!CODE [VbVbalrStatements#71](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#71)]  
  
### Implicit Line Continuation  
 In many cases, you can continue a statement on the next consecutive line without using the underscore character (_). The following table lists the syntax elements that implicitly continue the statement on the next line of code.  
  
|||  
|-|-|  
|Syntax element|Example|  
|After a comma (`,`).|[!CODE [VbVbalrLineContinuation#1](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#1)]|  
|After an open parenthesis (`(`) or before a closing parenthesis (`)`).|[!CODE [VbVbalrLineContinuation#2](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#2)]|  
|After an open curly brace (`{`) or before a closing curly brace (`}`).|[!CODE [VbVbalrLineContinuation#3](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#3)]<br /><br /> For more information, see [Object Initializers: Named and Anonymous Types](../vs140/Object-Initializers--Named-and-Anonymous-Types--Visual-Basic-.md) or [Collection Initializers Overview](../Topic/Collection%20Initializers%20\(Visual%20Basic\).md).|  
|After an open embedded expression (`<%=`) or before the close of an embedded expression (`%>`) within an XML literal.|[!CODE [VbVbalrLineContinuation#4](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#4)]<br /><br /> For more information, see [Embedded Expressions In XML](../Topic/Embedded%20Expressions%20in%20XML%20\(Visual%20Basic\).md).|  
|After the concatenation operator (`&`).|[!CODE [VbVbcnConventions#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnConventions#9)]<br /><br /> For more information, see [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md).|  
|After assignment operators (`=`, `&=`, `:=`, `+=`, `-=`, `*=`, `/=`, `\=`, `^=`, `<<=`, `>>=`).|[!CODE [VbVbalrLineContinuation#5](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#5)]<br /><br /> For more information, see [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md).|  
|After binary operators (`+`, `-`, `/`, `*`, `Mod`, `<>`, `<`, `>`, `<=`, `>=`, `^`, `>>`, `<<`, `And`, `AndAlso`, `Or`, `OrElse`, `Like`, `Xor`) within an expression.|[!CODE [VbVbalrLineContinuation#7](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#7)]<br /><br /> For more information, see [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md).|  
|After the `Is` and `IsNot` operators.|[!CODE [VbVbalrLineContinuation#8](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#8)]<br /><br /> For more information, see [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md).|  
|After a member qualifier character (`.`) and before the member name. However, you must include a line-continuation character (_) following a member qualifier character when you are using the `With` statement or supplying values in the initialization list for a type. Consider breaking the line after the assignment operator (for example, `=`) when you are using `With` statements or object initialization lists.|[!CODE [VbVbalrLineContinuation#5](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#5)]<br />[!CODE [VbVbalrLineContinuation#14](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#14)]<br /><br /> For more information, see [With...End With Statement (Visual Basic)](../Topic/With...End%20With%20Statement%20\(Visual%20Basic\).md) or [Object Initializers: Named and Anonymous Types](../vs140/Object-Initializers--Named-and-Anonymous-Types--Visual-Basic-.md).|  
|After an XML axis property qualifier (`.` or `.@` or `...`). However, you must include a line-continuation character (_) when you specify a member qualifier when you are using the `With` keyword.|[!CODE [VbVbalrLineContinuation#9](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#9)]<br /><br /> For more information, see [XML Axis Properties](../Topic/XML%20Axis%20Properties%20\(Visual%20Basic\).md).|  
|After a less-than sign (<) or before a greater-than sign (`>`) when you specify an attribute. Also after a greater-than sign (`>`) when you specify an attribute. However, you must include a line-continuation character (_) when you specify assembly-level or module-level attributes.|[!CODE [VbVbalrLineContinuation#10](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#10)]<br /><br /> For more information, see [Attributes (C# and Visual Basic)](../vs140/Attributes--C#-and-Visual-Basic-.md).|  
|Before and after query operators (`Aggregate`, `Distinct`, `From`, `Group By`, `Group Join`, `Join`, `Let`, `Order By`, `Select`, `Skip`, `Skip While`, `Take`, `Take While`, `Where`, `In`, `Into`, `On`, `Ascending`, and `Descending`). You cannot break a line between the keywords of query operators that are made up of multiple keywords (`Order By`, `Group Join`, `Take While`, and `Skip While`).|[!CODE [VbVbalrLineContinuation#11](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#11)]<br /><br /> For more information, see [Queries (Visual Basic)](../vs140/Queries--Visual-Basic-.md).|  
|After the `In` keyword in a `For Each` statement.|[!CODE [VbVbalrLineContinuation#12](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#12)]<br /><br /> For more information, see [For Each...Next Statement (Visual Basic)](../Topic/For%20Each...Next%20Statement%20\(Visual%20Basic\).md).|  
|After the `From` keyword in a collection initializer.|[!CODE [VbVbalrLineContinuation#13](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#13)]<br /><br /> For more information, see [Collection Initializers Overview (Visual Basic)](../Topic/Collection%20Initializers%20\(Visual%20Basic\).md).|  
  
## Adding Comments  
 Source code is not always self-explanatory, even to the programmer who wrote it. To help document their code, therefore, most programmers make liberal use of embedded comments. Comments in code can explain a procedure or a particular instruction to anyone reading or working with it later. [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] ignores comments during compilation, and they do not affect the compiled code.  
  
 Comment lines begin with an apostrophe (`'`) or `REM` followed by a space. They can be added anywhere in code, except within a string. To append a comment to a statement, insert an apostrophe or `REM` after the statement, followed by the comment. Comments can also go on their own separate line. The following example demonstrates these possibilities.  
  
 [!CODE [VbVbalrStatements#72](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#72)]  
  
## Checking Compilation Errors  
 If, after you type a line of code, the line is displayed with a wavy blue underline (an error message may appear as well), there is a syntax error in the statement. You must find out what is wrong with the statement (by looking in the task list, or hovering over the error with the mouse pointer and reading the error message) and correct it. Until you have fixed all syntax errors in your code, your program will fail to compile correctly.  
  
## Related Sections  
  
|||  
|-|-|  
|Term|Definition|  
|[Assignment Operators](../vs140/Assignment-Operators--Visual-Basic-.md)|Provides links to language reference pages covering assignment operators such as `=`, `*=`, and `&=`.|  
|[Operators and Expressions in Visual Basic](../vs140/Operators-and-Expressions-in-Visual-Basic.md)|Shows how to combine elements with operators to yield new values.|  
|[How to: Break and Combine Statements in Code](../vs140/How-to--Break-and-Combine-Statements-in-Code--Visual-Basic-.md)|Shows how to break a single statement into multiple lines and how to place multiple statements on the same line.|  
|[How to: Label Statements](../vs140/How-to--Label-Statements--Visual-Basic-.md)|Shows how to label a line of code.|