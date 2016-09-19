---
title: "Delegate Statement"
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
ms.assetid: f799c518-0817-40cc-ad0b-4da846fdba57
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Delegate Statement
Used to declare a delegate. A delegate is a reference type that refers to a `Shared` method of a type or to an instance method of an object. Any procedure with matching parameter and return types can be used to create an instance of this delegate class. The procedure can then later be invoked by means of the delegate instance.  
  
## Syntax  
  
```  
[ <attrlist> ] [ accessmodifier ] _  
[ Shadows ] Delegate [ Sub | Function ] name [( Of typeparamlist )] [([ parameterlist ])] [ As type ]  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`attrlist`|Optional. List of attributes that apply to this delegate. Multiple attributes are separated by commas. You must enclose the [Attribute List](../vs140/Attribute-List--Visual-Basic-.md) in angle brackets ("`<`" and "`>`").|  
|`accessmodifier`|Optional. Specifies what code can access the delegate. Can be one of the following:<br /><br /> -   [Public](../vs140/Public--Visual-Basic-.md). Any code that can access the element that declares the delegate can access it.<br />-   [Protected](../vs140/Protected--Visual-Basic-.md). Only code within the delegate's class or a derived class can access it.<br />-   [Friend](../Topic/Friend%20\(Visual%20Basic\).md). Only code within the same assembly can access the delegate.<br />-   [Private](../vs140/Private--Visual-Basic-.md). Only code within the element that declares the delegate can access it.<br /><br /> You can specify `Protected Friend` to enable access from code within the delegate's class, a derived class, or the same assembly.|  
|`Shadows`|Optional. Indicates that this delegate redeclares and hides an identically named programming element, or set of overloaded elements, in a base class. You can shadow any kind of declared element with any other kind.<br /><br /> A shadowed element is unavailable from within the derived class that shadows it, except from where the shadowing element is inaccessible. For example, if a `Private` element shadows a base class element, code that does not have permission to access the `Private` element accesses the base class element instead.|  
|`Sub`|Optional, but either `Sub` or `Function` must appear. Declares this procedure as a delegate `Sub` procedure that does not return a value.|  
|`Function`|Optional, but either `Sub` or `Function` must appear. Declares this procedure as a delegate `Function` procedure that returns a value.|  
|`name`|Required. Name of the delegate type; follows standard variable naming conventions.|  
|`typeparamlist`|Optional. List of type parameters for this delegate. Multiple type parameters are separated by commas. Optionally, each type parameter can be declared variant by using `In` and `Out` generic modifiers. You must enclose the [Type List](../vs140/Type-List--Visual-Basic-.md) in parentheses and introduce it with the `Of` keyword.|  
|`parameterlist`|Optional. List of parameters that are passed to the procedure when it is called. You must enclose the [Parameter List](../Topic/Parameter%20List%20\(Visual%20Basic\).md) in parentheses.|  
|`type`|Required if you specify a `Function` procedure. Data type of the return value.|  
  
## Remarks  
 The `Delegate` statement defines the parameter and return types of a delegate class. Any procedure with matching parameters and return types can be used to create an instance of this delegate class. The procedure can then later be invoked by means of the delegate instance, by calling the delegate's `Invoke` method.  
  
 Delegates can be declared at the namespace, module, class, or structure level, but not within a procedure.  
  
 Each delegate class defines a constructor that is passed the specification of an object method. An argument to a delegate constructor must be a reference to a method, or a lambda expression.  
  
 To specify a reference to a method, use the following syntax:  
  
 `AddressOf` [`expression`.]`methodname`  
  
 The compile-time type of the `expression` must be the name of a class or an interface that contains a method of the specified name whose signature matches the signature of the delegate class. The `methodname` can be either a shared method or an instance method. The `methodname` is not optional, even if you create a delegate for the default method of the class.  
  
 To specify a lambda expression, use the following syntax:  
  
 `Function` ([`parm` As `type`, `parm2` As `type2`, ...]) `expression`  
  
 The signature of the function must match that of the delegate type. For more information about lambda expressions, see [Lambda Expressions](../vs140/Lambda-Expressions--Visual-Basic-.md).  
  
 For more information about delegates, see [Delegates (Visual Basic)](../Topic/Delegates%20\(Visual%20Basic\).md).  
  
## Example  
 The following example uses the `Delegate` statement to declare a delegate for operating on two numbers and returning a number. The `DelegateTest` method takes an instance of a delegate of this type and uses it to operate on pairs of numbers.  
  
 [!CODE [VbVbalrDelegates#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#14)]  
  
## See Also  
 [AddressOf Operator](../vs140/AddressOf-Operator--Visual-Basic-.md)   
 [Of](../Topic/Of%20Clause%20\(Visual%20Basic\).md)   
 [Delegates (Visual Basic)](../Topic/Delegates%20\(Visual%20Basic\).md)   
 [How to: Use a Generic Class](../Topic/How%20to:%20Use%20a%20Generic%20Class%20\(Visual%20Basic\).md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Covariance and Contravariance (C# and Visual Basic)](../vs140/Covariance-and-Contravariance--C#-and-Visual-Basic-.md)   
 [in (Generic Modifier) (Visual Basic)](../Topic/In%20\(Generic%20Modifier\)%20\(Visual%20Basic\).md)   
 [Out (Generic Modifier) (Visual Basic)](../Topic/Out%20\(Generic%20Modifier\)%20\(Visual%20Basic\).md)