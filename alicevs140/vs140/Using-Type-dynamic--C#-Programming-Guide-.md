---
title: "Using Type dynamic (C# Programming Guide)"
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
ms.assetid: 3828989d-c967-4a51-b948-857ebc8fdf26
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Type dynamic (C# Programming Guide)
[!INCLUDE[csharp_dev10_long](../vs140/includes/csharp_dev10_long_md.md)] introduces a new type, `dynamic`. The type is a static type, but an object of type `dynamic` bypasses static type checking. In most cases, it functions like it has type `object`. At compile time, an element that is typed as `dynamic` is assumed to support any operation. Therefore, you do not have to be concerned about whether the object gets its value from a COM API, from a dynamic language such as IronPython, from the HTML Document Object Model (DOM), from reflection, or from somewhere else in the program. However, if the code is not valid, errors are caught at run time.  
  
 For example, if instance method `exampleMethod1` in the following code has only one parameter, the compiler recognizes that the first call to the method, `ec.exampleMethod1(10, 4)`, is not valid because it contains two arguments. The call causes a compiler error. The second call to the method, `dynamic_ec.exampleMethod1(10, 4)`, is not checked by the compiler because the type of `dynamic_ec` is `dynamic`. Therefore, no compiler error is reported. However, the error does not escape notice indefinitely. It is caught at run time and causes a run-time exception.  
  
 [!CODE [CsProgGuideTypes#50](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#50)]  
  
 [!CODE [CsProgGuideTypes#56](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#56)]  
  
 The role of the compiler in these examples is to package together information about what each statement is proposing to do to the object or expression that is typed as `dynamic`. At run time, the stored information is examined, and any statement that is not valid causes a run-time exception.  
  
 The result of most dynamic operations is itself `dynamic`. For example, if you rest the mouse pointer over the use of `testSum` in the following example, IntelliSense displays the type **(local variable) dynamic testSum**.  
  
 [!CODE [CsProgGuideTypes#51](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#51)]  
  
 Operations in which the result is not `dynamic` include conversions from `dynamic` to another type, and constructor calls that include arguments of type `dynamic`. For example, the type of `testInstance` in the following declaration is `ExampleClass`, not `dynamic`.  
  
 [!CODE [CsProgGuideTypes#52](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#52)]  
  
 Conversion examples are shown in the following section, "Conversions."  
  
## Conversions  
 Conversions between dynamic objects and other types are easy. This enables the developer to switch between dynamic and non-dynamic behavior.  
  
 Any object can be converted to dynamic type implicitly, as shown in the following examples.  
  
 [!CODE [CsProgGuideTypes#53](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#53)]  
  
 Conversely, an implicit conversion can be dynamically applied to any expression of type `dynamic`.  
  
 [!CODE [CsProgGuideTypes#54](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#54)]  
  
## Overload Resolution with Arguments of Type dynamic  
 Overload resolution occurs at run time instead of at compile time if one or more of the arguments in a method call have the type `dynamic`, or if the receiver of the method call is of type `dynamic`. In the following example, if the only accessible `exampleMethod2` method is defined to take a string argument, sending `d1` as the argument does not cause a compiler error, but it does cause a run-time exception. Overload resolution fails at run time because the run-time type of `d1` is `int`, and `exampleMethod2` requires a string.  
  
 [!CODE [CsProgGuideTypes#55](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#55)]  
  
## Dynamic Language Runtime  
 The dynamic language runtime (DLR) is a new API in [!INCLUDE[net_v40_short](../vs140/includes/net_v40_short_md.md)]. It provides the infrastructure that supports the `dynamic` type in C#, and also the implementation of dynamic programming languages such as IronPython and IronRuby. For more information about the DLR, see [Dynamic Language Runtime Overview](assetId:///f769a271-8aff-4bea-bfab-6160217ce23d).  
  
## COM Interop  
 [!INCLUDE[csharp_dev10_long](../vs140/includes/csharp_dev10_long_md.md)] includes several features that improve the experience of interoperating with COM APIs such as the Office Automation APIs. Among the improvements are the use of the `dynamic` type, and of [named and optional arguments](../Topic/Named%20and%20Optional%20Arguments%20\(C%23%20Programming%20Guide\).md).  
  
 Many COM methods allow for variation in argument types and return type by designating the types as `object`. This has necessitated explicit casting of the values to coordinate with strongly typed variables in C#. If you compile by using the [/link](../Topic/-link%20\(C%23%20Compiler%20Options\).md) option, the introduction of the `dynamic` type enables you to treat the occurrences of `object` in COM signatures as if they were of type `dynamic`, and thereby to avoid much of the casting. For example, the following statements contrast how you access a cell in a Microsoft Office Excel spreadsheet with the `dynamic` type and without the `dynamic` type.  
  
 [!CODE [csOfficeWalkthrough#12](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#12)]  
  
 [!CODE [csOfficeWalkthrough#13](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#13)]  
  
## Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[dynamic (C# Reference)](../vs140/dynamic--C#-Reference-.md)|Describes the usage of the `dynamic` keyword.|  
|[Dynamic Language Runtime Overview](assetId:///f769a271-8aff-4bea-bfab-6160217ce23d)|Provides an overview of the DLR, which is a runtime environment that adds a set of services for dynamic languages to the common language runtime (CLR).|  
|[Walkthrough: Creating and Using Dynamic Objects (C# and Visual Basic)](../Topic/Walkthrough:%20Creating%20and%20Using%20Dynamic%20Objects%20\(C%23%20and%20Visual%20Basic\).md)|Provides step-by-step instructions for creating a custom dynamic object and for creating a project that accesses an `IronPython` library.|  
|[How to: Access Office Interop Objects by Using Visual C# 2010](../Topic/How%20to:%20Access%20Office%20Interop%20Objects%20by%20Using%20Visual%20C%23%20Features%20\(C%23%20Programming%20Guide\).md)|Demonstrates how to create a project that uses named and optional arguments, the `dynamic` type, and other enhancements that simplify access to Office API objects.|