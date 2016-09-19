---
title: "Refactoring and Rename Dialog Box (Visual Basic)"
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
ms.assetid: 001d2d81-9bb6-4e8e-ae3a-20c0daaa3959
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Refactoring and Rename Dialog Box (Visual Basic)
Use Visual Basic's built-in **Rename** dialog box to rename identifiers in your code for symbols such as fields, local variables, methods, namespaces, properties, and types. You can open the **Rename** dialog box by right-clicking the element declaration.  
  
 **New Name**  
 Specifies the new name for the code element.  
  
 **Location**  
 Identifies the namespace to search when you perform the rename operation.  
  
## Rename Operations  
 The **Rename** dialog box performs slightly different rename operations, depending on the type of the element renamed.  
  
|Element type|Rename Operation|  
|------------------|----------------------|  
|Class|Changes all declarations and all usages of the class to the new name. For partial classes, the rename operation propagates to all parts.|  
|Field|Changes the declaration and usages of the field to the new name.|  
|Local variable|Changes the declaration and usages of the variable to the new name.|  
|Method|Changes the name of the method and all references to that method to the new name.|  
|Namespace|Changes the name of the namespace to the new name, in the declaration, all `Imports` statements, and all fully qualified names.|  
|Property|Changes the declaration and usages of the property to the new name.|  
  
## Refactoring  
 To provide a complete refactoring experience, Visual Basic has partnered with Developer Express Inc. to obtain refactoring support. See [Refactor!](http://go.microsoft.com/fwlink/?LinkId=155788) on the MSDN Visual Basic Developer Center for additional details and instructions on how to download this tool. Refactor! supports more than 15 individual refactoring features. This includes operations such as Reorder Parameters, Extract Method, Encapsulate Field, and Create Overload.  
  
## See Also  
 [Using the Visual Basic Editor](../vs140/Using-the-Visual-Basic-Development-Environment.md)