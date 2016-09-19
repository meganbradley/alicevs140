---
title: "Option Strict Statement"
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
ms.assetid: 5883e0c1-a920-4274-8e46-b0ff047eaee5
caps.latest.revision: 51
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict Statement
Restricts implicit data type conversions to only widening conversions, disallows late binding, and disallows implicit typing that results in an `Object` type.  
  
## Syntax  
  
```  
Option Strict { On | Off }  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`On`|Optional. Enables `Option Strict` checking.|  
|`Off`|Optional. Disables `Option Strict` checking.|  
  
## Remarks  
 When `Option Strict On` or `Option Strict` appears in a file, the following conditions cause a compile-time error:  
  
-   Implicit narrowing conversions  
  
-   Late binding  
  
-   Implicit typing that results in an `Object` type  
  
> [!NOTE]
>  In the warning configurations that you can set on the [Compile Page, Project Designer (Visual Basic)](../vs140/Compile-Page--Project-Designer--Visual-Basic-.md), there are three settings that correspond to the three conditions that cause a compile-time error. For information about how to use these settings, see [To set warning configurations in the IDE](../vs140/Option-Strict-Statement.md#conditions) later in this topic.  
  
 The `Option Strict Off` statement turns off error and warning checking for all three conditions, even if the associated IDE settings specify to turn on these errors or warnings. The `Option Strict On` statement turns on error and warning checking for all three conditions, even if the associated IDE settings specify to turn off these errors or warnings.  
  
 If used, the `Option Strict` statement must appear before any other code statements in a file.  
  
 When you set `Option Strict` to `On`, Visual Basic checks that data types are specified for all programming elements. Data types can be specified explicitly, or specified by using local type inference. Specifying data types for all your programming elements is recommended, for the following reasons:  
  
-   It enables IntelliSense support for your variables and parameters. This enables you to see their properties and other members as you type code.  
  
-   It enables the compiler to perform type checking. Type checking helps you find statements that can fail at run time because of type conversion errors. It also identifies calls to methods on objects that do not support those methods.  
  
-   It speeds up the execution of code. One reason for this is that if you do not specify a data type for a programming element, the Visual Basic compiler assigns it the `Object` type. Compiled code might have to convert back and forth between `Object` and other data types, which reduces performance.  
  
## Implicit Narrowing Conversion Errors  
 Implicit narrowing conversion errors occur when there is an implicit data type conversion that is a narrowing conversion.  
  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] can convert many data types to other data types. Data loss can occur when the value of one data type is converted to a data type that has less precision or a smaller capacity. A run-time error occurs if such a narrowing conversion fails. `Option Strict` ensures compile-time notification of these narrowing conversions so that you can avoid them. For more information, see [Implicit and Explicit Conversions (Visual Basic)](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md) and [Widening and Narrowing Conversions (Visual Basic)](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md).  
  
 Conversions that can cause errors include implicit conversions that occur in expressions. For more information, see the following topics:  
  
-   [+ Operator (Visual Basic)](../Topic/+%20Operator%20\(Visual%20Basic\).md)  
  
-   [+= Operator (Visual Basic)](../vs140/-=-Operator--Visual-Basic-.md)  
  
-   [\ Operator (Visual Basic)](../Topic/-%20Operator%20\(Visual%20Basic\)2.md)  
  
-   [/= Operator (Visual Basic)](../vs140/-=-Operator--Visual-Basic-1.md)  
  
-   [Char Data Type (Visual Basic)](../vs140/Char-Data-Type--Visual-Basic-.md)  
  
 When you concatenate strings by using the [& Operator (Visual Basic)](../Topic/&%20Operator%20\(Visual%20Basic\).md), all conversions to the strings are considered to be widening. So these conversions do not generate an implicit narrowing conversion error, even if `Option Strict` is on.  
  
 When you call a method that has an argument that has a data type different from the corresponding parameter, a narrowing conversion causes a compile-time error if `Option Strict` is on. You can avoid the compile-time error by using a widening conversion or an explicit conversion.  
  
 Implicit narrowing conversion errors are suppressed at compile-time for conversions from the elements in a `For Each…Next` collection to the loop control variable. This occurs even if `Option Strict` is on. For more information, see the "Narrowing Conversions" section in [For Each…Next Statement](../Topic/For%20Each...Next%20Statement%20\(Visual%20Basic\).md).  
  
## Late Binding Errors  
 An object is late bound when it is assigned to a property or method of a variable that is declared to be of type `Object`. For more information, see [Early and Late Binding (Visual Basic)](../vs140/Early-and-Late-Binding--Visual-Basic-.md).  
  
## Implicit Object Type Errors  
 Implicit object type errors occur when an appropriate type cannot be inferred for a declared variable, so a type of `Object` is inferred. This primarily occurs when you use a `Dim` statement to declare a variable without using an `As` clause, and `Option Infer` is off. For more information, see [Option Infer Statement](../vs140/Option-Infer-Statement.md) and the [Visual Basic Language Specification](../vs140/Visual-Basic-Language-Specification.md).  
  
 For method parameters, the `As` clause is optional if `Option Strict` is off. However, if any one parameter uses an `As` clause, they all must use it. If `Option Strict` is on, the `As` clause is required for every parameter definition.  
  
 If you declare a variable without using an `As` clause and set it to `Nothing`, the variable has a type of `Object`. No compile-time error occurs in this case when `Option Strict` is on and `Option Infer` is on. An example of this is `Dim something = Nothing`.  
  
### Default Data Types and Values  
 The following table describes the results of various combinations of specifying the data type and initializer in a [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md).  
  
|||||  
|-|-|-|-|  
|Data type specified?|Initializer specified?|Example|Result|  
|No|No|`Dim qty`|If `Option Strict` is off (the default), the variable is set to `Nothing`.<br /><br /> If `Option Strict` is on, a compile-time error occurs.|  
|No|Yes|`Dim qty = 5`|If `Option Infer` is on (the default), the variable takes the data type of the initializer. See [Local Type Inference (Visual Basic)](../vs140/Local-Type-Inference--Visual-Basic-.md).<br /><br /> If `Option Infer` is off and `Option Strict` is off, the variable takes the data type of `Object`.<br /><br /> If `Option Infer` is off and `Option Strict` is on, a compile-time error occurs.|  
|Yes|No|`Dim qty As Integer`|The variable is initialized to the default value for the data type. For more information, see [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md).|  
|Yes|Yes|`Dim qty  As Integer = 5`|If the data type of the initializer is not convertible to the specified data type, a compile-time error occurs.|  
  
## When an Option Strict Statement Is Not Present  
 If the source code does not contain an `Option Strict` statement, the **Option strict** setting on the [Compile Page, Project Designer (Visual Basic)](../vs140/Compile-Page--Project-Designer--Visual-Basic-.md) is used. The **Compile Page** has settings that provide additional control over the conditions that generate an error.  
  
 If you are using the command-line compiler, you can use the [/optionstrict](../vs140/-optionstrict.md) compiler option to specify a setting for `Option Strict`.  
  
### To set Option Strict in the IDE  
 [!INCLUDE[note_settings_general](../vs140/includes/note_settings_general_md.md)]  
  
1.  In **Solution Explorer**, select a project. On the **Project** menu, click **Properties**. For more information, see [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7).  
  
2.  On the **Compile** tab, set the value in the **Option Strict** box.  
  
###  <a name="conditions"></a> To set warning configurations in the IDE  
 When you use the [Compile Page, Project Designer (Visual Basic)](../vs140/Compile-Page--Project-Designer--Visual-Basic-.md) instead of an `Option Strict` statement, you have additional control over the conditions that generate errors. The **Warning configurations** section of the **Compile Page** has settings that correspond to the three conditions that cause a compile-time error when `Option Strict` is on. Following are these settings:  
  
-   **Implicit conversion**  
  
-   **Late binding; call could fail at run time**  
  
-   **Implicit type; object assumed**  
  
 When you set **Option Strict** to **On**, all three of these warning configuration settings are set to **Error**. When you set **Option Strict** to **Off**, all three settings are set to **None**.  
  
 You can individually change each warning configuration setting to **None**, **Warning**, or **Error**. If all three warning configuration settings are set to **Error**, `On` appears in the `Option strict` box. If all three are set to **None**, `Off` appears in this box. For any other combination of these settings, **(custom)** appears.  
  
### To set the Option Strict default setting for new projects  
 When you create a project, the **Option Strict** setting on the **Compile** tab is set to the **Option Strict** setting in the **Options** dialog box.  
  
 To set `Option Strict` in this dialog box, on the **Tools** menu, click **Options**. In the **Options** dialog box, expand **Projects and Solutions**, and then click **VB Defaults**. The initial default setting in **VB Defaults** is `Off`.  
  
### To set Option Strict on the command line  
 Include the [/optionstrict](../vs140/-optionstrict.md) compiler option in the **vbc** command.  
  
## Example  
 The following examples demonstrate compile-time errors caused by implicit type conversions that are narrowing conversions. This category of errors corresponds to the **Implicit conversion** condition on the **Compile Page**.  
  
 [!CODE [VbVbalrStatements#161](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#161)]  
  
## Example  
 The following example demonstrates a compile-time error caused by late binding. This category of errors corresponds to the **Late binding; call could fail at run time** condition on the **Compile Page**.  
  
 [!CODE [VbVbalrStatements#162](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#162)]  
  
## Example  
 The following examples demonstrate errors caused by variables that are declared with an implicit type of `Object`. This category of errors corresponds to the **Implicit type; object assumed** condition on the **Compile Page**.  
  
 [!CODE [VbVbalrStatements#163](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#163)]  
  
 [!CODE [VbVbalrStatements#164](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#164)]  
  
## See Also  
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [Implicit and Explicit Conversions (Visual Basic)](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)   
 [Compile Page, Project Designer (Visual Basic)](../vs140/Compile-Page--Project-Designer--Visual-Basic-.md)   
 [Option Explicit Statement](../vs140/Option-Explicit-Statement--Visual-Basic-.md)   
 [Type Conversion Functions (Visual Basic)](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [How to: Access Members of an Object (Visual Basic)](../Topic/How%20to:%20Access%20Members%20of%20an%20Object%20\(Visual%20Basic\).md)   
 [Embedded Expressions in XML (Visual Basic)](../Topic/Embedded%20Expressions%20in%20XML%20\(Visual%20Basic\).md)   
 [Relaxed Delegate Conversion (Visual Basic)](../vs140/Relaxed-Delegate-Conversion--Visual-Basic-.md)   
 [Late Binding in Office Solutions](assetId:///80b0d23e-df68-4ea9-a02b-238aee8ca9c0)   
 [/optionstrict](../vs140/-optionstrict.md)   
 [Visual Basic Defaults, Projects, Options Dialog Box](../vs140/Visual-Basic-Defaults--Projects--Options-Dialog-Box.md)