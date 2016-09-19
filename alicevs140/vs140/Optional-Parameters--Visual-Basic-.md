---
title: "Optional Parameters (Visual Basic)"
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
ms.assetid: 398d2845-1069-4e94-b934-a73b545c8b87
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Optional Parameters (Visual Basic)
You can specify that a procedure parameter is optional and no argument has to be supplied for it when the procedure is called. *Optional parameters* are indicated by the `Optional` keyword in the procedure definition. The following rules apply:  
  
-   Every optional parameter in the procedure definition must specify a default value.  
  
-   The default value for an optional parameter must be a constant expression.  
  
-   Every parameter following an optional parameter in the procedure definition must also be optional.  
  
 The following syntax shows a procedure declaration with an optional parameter:  
  
```  
Sub sub name(ByVal parameter1 As datatype1, Optional ByVal parameter2 As datatype2 = defaultvalue)  
```  
  
## Calling Procedures with Optional Parameters  
 When you call a procedure with an optional parameter, you can choose whether to supply the argument. If you do not, the procedure uses the default value declared for that parameter.  
  
 When you omit one or more optional arguments in the argument list, you use successive commas to mark their positions. The following example call supplies the first and fourth arguments but not the second or third:  
  
```  
  
sub name(argument 1, , , argument 4)  
```  
  
 The following example makes several calls to the `MsgBox` function. `MsgBox` has one required parameter and two optional parameters.  
  
 The first call to `MsgBox` supplies all three arguments in the order that `MsgBox` defines them. The second call supplies only the required argument. The third and fourth calls supply the first and third arguments. The third call does this by position, and the fourth call does it by name.  
  
 [!CODE [VbVbcnProcedures#47](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#47)]  
  
## Determining Whether an Optional Argument Is Present  
 A procedure cannot detect at run time whether a given argument has been omitted or the calling code has explicitly supplied the default value. If you need to make this distinction, you can set an unlikely value as the default. The following procedure defines the optional parameter `office`, and tests for its default value, `QJZ`, to see if it has been omitted in the call:  
  
 [!CODE [VbVbcnProcedures#46](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#46)]  
  
 If the optional parameter is a reference type such as a `String`, you can use `Nothing` as the default value, provided this is not an expected value for the argument.  
  
## Optional Parameters and Overloading  
 Another way to define a procedure with optional parameters is to use overloading. If you have one optional parameter, you can define two overloaded versions of the procedure, one accepting the parameter and one without it. This approach becomes more complicated as the number of optional parameters increases. However, its advantage is that you can be absolutely sure whether the calling program supplied each optional argument.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Argument Passing By Value and By Reference](../vs140/Passing-Arguments-by-Value-and-by-Reference--Visual-Basic-.md)   
 [Passing Arguments by Position and by Name](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md)   
 [Parameter Arrays](../Topic/Parameter%20Arrays%20\(Visual%20Basic\).md)   
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Optional](../vs140/Optional--Visual-Basic-.md)   
 [ParamArray](../vs140/ParamArray--Visual-Basic-.md)