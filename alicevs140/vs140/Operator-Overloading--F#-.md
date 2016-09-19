---
title: "Operator Overloading (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 6217a7e4-863b-475a-9d79-b788cddfb6f9
caps.latest.revision: 34
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operator Overloading (F#)
This topic describes how to overload arithmetic operators in a class or record type, and at the global level.  
  
## Syntax  
  
```  
// Overloading an operator as a class or record member.   
static member (operator-symbols) (parameter-list) =   
    method-body  
// Overloading an operator at the global level  
let [inline] (operator-symbols) parameter-list =  
    function-body  
```  
  
## Remarks  
 In the previous syntax, the `operator-symbol` is one of `+`, `-`, `*`, `/`, `=`, and so on. The `parameter-list` specifies the operands in the order they appear in the usual syntax for that operator. The `method-body` constructs the resulting value.  
  
 Operator overloads for operators must be static. Operator overloads for unary operators, such as `+` and `-`, must use a tilde (`~`) in the `operator-symbol` to indicate that the operator is a unary operator and not a binary operator, as shown in the following declaration.  
  
```f#  
static member (~-) (v : Vector)  
```  
  
 The following code illustrates a vector class that has just two operators, one for unary minus and one for multiplication by a scalar. In the example, two overloads for scalar multiplication are needed because the operator must work regardless of the order in which the vector and scalar appear.  
  
 [!CODE [FsLangRef2#4001](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#4001)]  
  
## Creating New Operators  
 You can overload all the standard operators, but you can also create new operators out of sequences of certain characters. Allowed operator characters are `!`, `%`, `&`, `*`, `+`, `-`, `.`, `/`, `<`, `=`, `>`, `?`, `@`, `^`, `|`, and `~`. The `~` character has the special meaning of making an operator unary, and is not part of the operator character sequence. Not all operators can be made unary, as is described in [Prefix and Infix Operators](#prefix) later in this topic.  
  
 Depending on the exact character sequence you use, your operator will have a certain precedence and associativity. Associativity can be either left to right or right to left and is used whenever operators of the same level of precedence appear in sequence without parentheses.  
  
 The operator character `.` does not affect precedence, so that, for example, if you want to define your own version of multiplication that has the same precedence and associativity as ordinary multiplication, you could create operators such as `.*`.  
  
 A table that shows the precedence of all operators in F# can be found in [Symbol and Operator Reference](../vs140/Symbol-and-Operator-Reference--F#-.md).  
  
## Overloaded Operator Names  
 When the F# compiler compiles an operator expression, it generates a method that has a compiler-generated name for that operator. This is the name that appears in the Microsoft intermediate language (MSIL) for the method, and also in reflection and IntelliSense. You do not normally need to use these names in F# code.  
  
 The following table shows the standard operators and their corresponding generated names.  
  
|Operator|Generated name|  
|--------------|--------------------|  
|`[]`|`op_Nil`|  
|`::`|`op_Cons`|  
|`+`|`op_Addition`|  
|`-`|`op_Subtraction`|  
|`*`|`op_Multiply`|  
|`/`|`op_Division`|  
|`@`|`op_Append`|  
|`^`|`op_Concatenate`|  
|`%`|`op_Modulus`|  
|`&&&`|`op_BitwiseAnd`|  
|`&#124;&#124;&#124;`|`op_BitwiseOr`|  
|`^^^`|`op_ExclusiveOr`|  
|`<<<`|`op_LeftShift`|  
|`~~~`|`op_LogicalNot`|  
|`>>>`|`op_RightShift`|  
|`~+`|`op_UnaryPlus`|  
|`~-`|`op_UnaryNegation`|  
|`=`|`op_Equality`|  
|`<=`|`op_LessThanOrEqual`|  
|`>=`|`op_GreaterThanOrEqual`|  
|`<`|`op_LessThan`|  
|`>`|`op_GreaterThan`|  
|`?`|`op_Dynamic`|  
|`?<-`|`op_DynamicAssignment`|  
|`&#124;>`|`op_PipeRight`|  
|`<&#124;`|`op_PipeLeft`|  
|`!`|`op_Dereference`|  
|`>>`|`op_ComposeRight`|  
|`<<`|`op_ComposeLeft`|  
|`<@ @>`|`op_Quotation`|  
|`<@@ @@>`|`op_QuotationUntyped`|  
|`+=`|`op_AdditionAssignment`|  
|`-=`|`op_SubtractionAssignment`|  
|`*=`|`op_MultiplyAssignment`|  
|`/=`|`op_DivisionAssignment`|  
|`..`|`op_Range`|  
|`.. ..`|`op_RangeStep`|  
  
 Other combinations of operator characters that are not listed here can be used as operators and have names that are made up by concatenating names for the individual characters from the following table. For example, +! becomes `op_PlusBang`.  
  
|Operator character|Name|  
|------------------------|----------|  
|`>`|`Greater`|  
|`<`|`Less`|  
|`+`|`Plus`|  
|`-`|`Minus`|  
|`*`|`Multiply`|  
|`/`|`Divide`|  
|`=`|`Equals`|  
|`~`|`Twiddle`|  
|`%`|`Percent`|  
|`.`|`Dot`|  
|`&`|`Amp`|  
|`&#124;`|`Bar`|  
|`@`|`At`|  
|`^`|`Hat`|  
|`!`|`Bang`|  
|`?`|`Qmark`|  
|`(`|`LParen`|  
|`,`|`Comma`|  
|`)`|`RParen`|  
|`[`|`LBrack`|  
|`]`|`RBrack`|  
  
##  <a name="prefix"></a> Prefix and Infix Operators  
 *Prefix* operators are expected to be placed in front of an operand or operands, much like a function. *Infix* operators are expected to be placed between the two operands.  
  
 Only certain operators can be used as prefix operators. Some operators are always prefix operators, others can be infix or prefix, and the rest are always infix operators. Operators that begin with `!`, except `!=`, and the operator `~`, or repeated sequences of`~`, are always prefix operators. The operators `+`, `-`, `+.`, `-.`, `&`, `&&`, `%`, and `%%` can be prefix operators or infix operators. You distinguish the prefix version of these operators from the infix version by adding a `~` at the beginning of a prefix operator when it is defined. The `~` is not used when you use the operator, only when it is defined.  
  
## Example  
 The following code illustrates the use of operator overloading to implement a fraction type. A fraction is represented by a numerator and a denominator. The function `hcf` is used to determine the highest common factor, which is used to reduce fractions.  
  
 [!CODE [FsLangRef2#4002](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#4002)]  
  
 **// Output:**  
**3/4 + 1/2 = 5/4**  
**3/4 - 1/2 = 1/4**  
**3/4 \* 1/2 = 3/8**  
**3/4 / 1/2 = 3/2**  
**3/4 + 1 = 7/4**   
## Operators at the Global Level  
 You can also define operators at the global level. The following code defines an operator +?.  
  
 [!CODE [FsLangRef2#4003](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#4003)]  
  
 The output of the above code is `12`.  
  
 You can redefine the regular arithmetic operators in this manner because the scoping rules for F# dictate that newly defined operators take precedence over the built-in operators.  
  
 The keyword `inline` is often used with global operators, which are often small functions that are best integrated into the calling code. Making operator functions inline also enables them to work with statically resolved type parameters to produce statically resolved generic code. For more information, see [Inline Functions](../vs140/Inline-Functions--F#-.md) and [Statically Resolved Type Parameters](../vs140/Statically-Resolved-Type-Parameters--F#-.md).  
  
## See Also  
 [Members](../vs140/Members--F#-.md)