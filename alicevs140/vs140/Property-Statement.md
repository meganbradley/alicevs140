---
title: "Property Statement"
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
ms.assetid: 3155edaf-8ebd-45c6-9cef-11d5d2dc8d38
caps.latest.revision: 43
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property Statement
Declares the name of a property, and the property procedures used to store and retrieve the value of the property.  
  
## Syntax  
  
```  
[ <attributelist> ] [ Default ] [ accessmodifier ]   
[ propertymodifiers ] [ Shared ] [ Shadows ] [ ReadOnly | WriteOnly ] [ Iterator ]  
Property name ( [ parameterlist ] ) [ As returntype ] [ Implements implementslist ]  
    [ <attributelist> ] [ accessmodifier ] Get  
        [ statements ]  
    End Get  
    [ <attributelist> ] [ accessmodifier ] Set ( ByVal value As returntype [, parameterlist ] )  
        [ statements ]  
    End Set  
End Property  
- or -  
[ <attributelist> ] [ Default ] [ accessmodifier ]   
[ propertymodifiers ] [ Shared ] [ Shadows ] [ ReadOnly | WriteOnly ]   
Property name ( [ parameterlist ] ) [ As returntype ] [ Implements implementslist ]  
  
```  
  
## Parts  
  
-   `attributelist`  
  
     Optional. List of attributes that apply to this property or `Get` or `Set` procedure. See [Attribute List](../vs140/Attribute-List--Visual-Basic-.md).  
  
-   `Default`  
  
     Optional. Specifies that this property is the default property for the class or structure on which it is defined. Default properties must accept parameters and can be set and retrieved without specifying the property name. If you declare the property as `Default`, you cannot use `Private` on the property or on either of its property procedures.  
  
-   `accessmodifier`  
  
     Optional on the `Property` statement and on at most one of the `Get` and `Set` statements. Can be one of the following:  
  
    -   [Public](../vs140/Public--Visual-Basic-.md)  
  
    -   [Protected](../vs140/Protected--Visual-Basic-.md)  
  
    -   [Friend](../Topic/Friend%20\(Visual%20Basic\).md)  
  
    -   [Private](../vs140/Private--Visual-Basic-.md)  
  
    -   `Protected Friend`  
  
     See [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md).  
  
-   `propertymodifiers`  
  
     Optional. Can be one of the following:  
  
    -   [Overloads](../vs140/Overloads--Visual-Basic-.md)  
  
    -   [Overrides](../vs140/Overrides--Visual-Basic-.md)  
  
    -   [Overridable](../vs140/Overridable--Visual-Basic-.md)  
  
    -   [NotOverridable](../vs140/NotOverridable--Visual-Basic-.md)  
  
    -   [MustOverride](../vs140/MustOverride--Visual-Basic-.md)  
  
    -   `MustOverride Overrides`  
  
    -   `NotOverridable Overrides`  
  
-   `Shared`  
  
     Optional. See [Shared](../Topic/Shared%20\(Visual%20Basic\).md).  
  
-   `Shadows`  
  
     Optional. See [Shadows](../vs140/Shadows--Visual-Basic-.md).  
  
-   `ReadOnly`  
  
     Optional. See [ReadOnly](../vs140/ReadOnly--Visual-Basic-.md).  
  
-   `WriteOnly`  
  
     Optional. See [WriteOnly](../vs140/WriteOnly--Visual-Basic-.md).  
  
-   `Iterator`  
  
     Optional. See [Iterator](../Topic/Iterator%20\(Visual%20Basic\).md).  
  
-   `name`  
  
     Required. Name of the property. See [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md).  
  
-   `parameterlist`  
  
     Optional. List of local variable names representing the parameters of this property, and possible additional parameters of the `Set` procedure. See [Parameter List](../Topic/Parameter%20List%20\(Visual%20Basic\).md).  
  
-   `returntype`  
  
     Required if `Option``Strict` is `On`. Data type of the value returned by this property.  
  
-   `Implements`  
  
     Optional. Indicates that this property implements one or more properties, each one defined in an interface implemented by this property's containing class or structure. See [Implements Statement](../vs140/Implements-Statement.md).  
  
-   `implementslist`  
  
     Required if `Implements` is supplied. List of properties being implemented.  
  
     `implementedproperty [ , implementedproperty ... ]`  
  
     Each `implementedproperty` has the following syntax and parts:  
  
     `interface.definedname`  
  
    |||  
    |-|-|  
    |Part|Description|  
    |`interface`|Required. Name of an interface implemented by this property's containing class or structure.|  
    |`definedname`|Required. Name by which the property is defined in `interface`.|  
  
-   `Get`  
  
     Optional. Required if the property is marked `WriteOnly`. Starts a `Get` property procedure that is used to return the value of the property.  
  
-   `statements`  
  
     Optional. Block of statements to run within the `Get` or `Set` procedure.  
  
-   `End Get`  
  
     Terminates the `Get` property procedure.  
  
-   `Set`  
  
     Optional. Required if the property is marked `ReadOnly`. Starts a `Set` property procedure that is used to store the value of the property.  
  
-   `End Set`  
  
     Terminates the `Set` property procedure.  
  
-   `End Property`  
  
     Terminates the definition of this property.  
  
## Remarks  
 The `Property` statement introduces the declaration of a property. A property can have a `Get` procedure (read only), a `Set` procedure (write only), or both (read-write). You can omit the `Get` and `Set` procedure when using an auto-implemented property. For more information, see [Auto-Implemented Properties](../vs140/Auto-Implemented-Properties--Visual-Basic-.md).  
  
 You can use `Property` only at class level. This means the *declaration context* for a property must be a class, structure, module, or interface, and cannot be a source file, namespace, procedure, or block. For more information, see [Declaration Contexts and Default Access Levels](../vs140/Declaration-Contexts-and-Default-Access-Levels--Visual-Basic-.md).  
  
 By default, properties use public access. You can adjust a property's access level with an access modifier on the `Property` statement, and you can optionally adjust one of its property procedures to a more restrictive access level.  
  
 Visual Basic passes a parameter to the `Set` procedure during property assignments. If you do not supply a parameter for `Set`, the integrated development environment (IDE) uses an implicit parameter named `value`. This parameter holds the value to be assigned to the property. You typically store this value in a private local variable and return it whenever the `Get` procedure is called.  
  
## Rules  
  
-   **Mixed Access Levels.** If you are defining a read-write property, you can optionally specify a different access level for either the `Get` or the `Set` procedure, but not both. If you do this, the procedure access level must be more restrictive than the property's access level. For example, if the property is declared `Friend`, you can declare the `Set` procedure `Private`, but not `Public`.  
  
     If you are defining a `ReadOnly` or `WriteOnly` property, the single property procedure (`Get` or `Set`, respectively) represents all of the property. You cannot declare a different access level for such a procedure, because that would set two access levels for the property.  
  
-   **Return Type.** The `Property` statement can declare the data type of the value it returns. You can specify any data type or the name of an enumeration, structure, class, or interface.  
  
     If you do not specify `returntype`, the property returns `Object`.  
  
-   **Implementation.** If this property uses the `Implements` keyword, the containing class or structure must have an `Implements` statement immediately following its `Class` or `Structure` statement. The `Implements` statement must include each interface specified in `implementslist`. However, the name by which an interface defines the `Property` (in `definedname`) does not have to be the same as the name of this property (in `name`).  
  
## Behavior  
  
-   **Returning from a Property Procedure.** When the `Get` or `Set` procedure returns to the calling code, execution continues with the statement following the statement that invoked it.  
  
     The `Exit Property` and `Return` statements cause an immediate exit from a property procedure. Any number of `Exit Property` and `Return` statements can appear anywhere in the procedure, and you can mix `Exit Property` and `Return` statements.  
  
-   **Return Value.** To return a value from a `Get` procedure, you can either assign the value to the property name or include it in a `Return` statement. The following example assigns the return value to the property name `quoteForTheDay` and then uses the `Exit Property` statement to return.  
  
     [!CODE [VbVbalrStatements#27](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#27)]  
  
     [!CODE [VbVbalrStatements#28](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#28)]  
  
     If you use `Exit Property` without assigning a value to `name`, the `Get` procedure returns the default value for the property's data type.  
  
     The `Return` statement at the same time assigns the `Get` procedure return value and exits the procedure. The following example shows this.  
  
     [!CODE [VbVbalrStatements#27](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#27)]  
  
     [!CODE [VbVbalrStatements#29](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#29)]  
  
## Example  
 The following example declares a property in a class.  
  
 [!CODE [VbVbalrStatements#51](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#51)]  
  
## See Also  
 [Auto-Implemented Properties](../vs140/Auto-Implemented-Properties--Visual-Basic-.md)   
 [Objects and Classes in Visual Basic](../Topic/Objects%20and%20Classes%20in%20Visual%20Basic.md)   
 [Get Statement](../vs140/Get-Statement.md)   
 [Set Statement](../vs140/Set-Statement--Visual-Basic-.md)   
 [Parameter List](../Topic/Parameter%20List%20\(Visual%20Basic\).md)   
 [Default (Visual Basic)](../vs140/Default--Visual-Basic-.md)