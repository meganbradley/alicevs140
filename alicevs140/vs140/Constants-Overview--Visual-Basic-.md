---
title: "Constants Overview (Visual Basic)"
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
ms.assetid: 29016fe8-78b3-4dc8-90b8-1cfec2fa8ac9
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Constants Overview (Visual Basic)
A constant is a meaningful name that takes the place of a number or string that does not change. Constants store values that, as the name implies, remain the same throughout the execution of an application. You can greatly improve the readability of your code and make it easier to maintain by using constants. Use them in code that contains values that reappear or that depends on certain numbers that are difficult to remember or have no obvious meaning.  
  
## How to Create and Use Constants  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] contains a number of predefined constants, mainly using for printing and displaying. You can also create your own constants with the `Const` statement, using the same guidelines you would for creating a variable name. If `Option Strict` is `On`, you must explicitly declare the constant type.  
  
 A constant's scope, which is the set of all code that can refer to it without qualifying its name, is the same as that of a variable declared in the same location. To create a constant that exists within the scope of a particular procedure, declare it inside that procedure. To create a constant that is available throughout an application, declare it using the `Public` keyword in the declarations section of the class.  
  
> [!NOTE]
>  Although constants somewhat resemble variables, you cannot modify them or assign new values to them as you can to variables.  
  
 The constants you use in your code can be defined by the object model for controls or components you work with, or they can be user-defined (that is, those you create yourself).  
  
## Compile-time and Run-time Constants  
 A compile-time constant is computed at the time the code is compiled, while a run-time constant can only be computed while the application is running. A compile-time constant will have the same value each time an application runs, while a run-time constant may change each time. Compile-time constants are required for cases such as array bounds, case expressions, or enumerator initializers.  
  
## In This Section  
  
|||  
|-|-|  
|Definition|Term|  
|[How to: Declare A Constant](../vs140/How-to--Declare-A-Constant--Visual-Basic-.md)|Explains how to use the `Const` statement to declare a constant and set its value; by declaring a constant, you assign a meaningful name to the value.|  
|[User-Defined Constants](../vs140/User-Defined-Constants--Visual-Basic-.md)|Describes how to create your own constants, including information on scoping and how to avoid circular references.|  
|[Constant and Literal Data Types](../vs140/Constant-and-Literal-Data-Types--Visual-Basic-.md)|Provides information on how the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler initializes constants when `Option Explicit` is turned off.|  
|[How to: Group Related Constant Values Together](../vs140/How-to--Group-Related-Constant-Values-Together--Visual-Basic-.md)|Demonstrates how to group constant values that are related.|  
  
## Reference  
  
|||  
|-|-|  
|Definition|Term|  
|[Constants and Enumerations (Visual Basic)](../Topic/Constants%20and%20Enumerations%20\(Visual%20Basic\).md)|Lists the constants predefined by [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)].|  
|[Const Statement (Visual Basic)](../Topic/Const%20Statement%20\(Visual%20Basic\).md)|Describes the `Const` statement and its use.|  
|[Option Strict Statement](../vs140/Option-Strict-Statement.md)|Describes the `Option Strict` statement and its use.|  
  
## See Also  
 [Enumerations Overview](../vs140/Enumerations-Overview--Visual-Basic-.md)   
 [How to: Initialize Array Variables in Visual Basic](../vs140/How-to--Initialize-an-Array-Variable-in-Visual-Basic.md)