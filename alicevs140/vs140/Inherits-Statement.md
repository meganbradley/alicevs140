---
title: "Inherits Statement"
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
ms.assetid: 9e6fe042-9af3-4341-8093-fc3537770cf2
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Inherits Statement
Causes the current class or interface to inherit the attributes, variables, properties, procedures, and events from another class or set of interfaces.  
  
## Syntax  
  
```  
Inherits basetypenames  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`basetypenames`|Required. The name of the class from which this class derives.<br /><br /> -or-<br /><br /> The names of the interfaces from which this interface derives. Use commas to separate multiple names.|  
  
## Remarks  
 If used, the `Inherits` statement must be the first non-blank, non-comment line in a class or interface definition. It should immediately follow the `Class` or `Interface` statement.  
  
 You can use `Inherits` only in a class or interface. This means the declaration context for an inheritance cannot be a source file, namespace, structure, module, procedure, or block.  
  
## Rules  
  
-   **Class Inheritance.** If a class uses the `Inherits` statement, you can specify only one base class.  
  
     A class cannot inherit from a class nested within it.  
  
-   **Interface Inheritance.** If an interface uses the `Inherits` statement, you can specify one or more base interfaces. You can inherit from two interfaces even if they each define a member with the same name. If you do so, the implementing code must use name qualification to specify which member it is implementing.  
  
     An interface cannot inherit from another interface with a more restrictive access level. For example, a `Public` interface cannot inherit from a `Friend` interface.  
  
     An interface cannot inherit from an interface nested within it.  
  
 An example of class inheritance in the .NET Framework is the <xref:System.ArgumentException?qualifyHint=False> class, which inherits from the <xref:System.SystemException?qualifyHint=False> class. This provides to <xref:System.ArgumentException?qualifyHint=False> all the predefined properties and procedures required by system exceptions, such as the <xref:System.Exception.Message?qualifyHint=False> property and the <xref:System.Exception.ToString?qualifyHint=False> method.  
  
 An example of interface inheritance in the .NET Framework is the <xref:System.Collections.ICollection?qualifyHint=False> interface, which inherits from the <xref:System.Collections.IEnumerable?qualifyHint=False> interface. This causes <xref:System.Collections.ICollection?qualifyHint=False> to inherit the definition of the enumerator required to traverse a collection.  
  
## Example  
 The following example uses the `Inherits` statement to show how a class named `thisClass` can inherit all the members of a base class named `anotherClass`.  
  
 [!CODE [VbVbalrStatements#37](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#37)]  
  
## Example  
 The following example shows inheritance of multiple interfaces.  
  
 [!CODE [VbVbalrStatements#38](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#38)]  
  
 The interface named `thisInterface` now includes all the definitions in the <xref:System.IComparable?qualifyHint=False>, <xref:System.IDisposable?qualifyHint=False>, and <xref:System.IFormattable?qualifyHint=False> interfaces The inherited members provide respectively for type-specific comparison of two objects, releasing allocated resources, and expressing the value of an object as a `String`. A class that implements `thisInterface` must implement every member of every base interface.  
  
## See Also  
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)   
 [NotInheritable](../vs140/NotInheritable--Visual-Basic-.md)   
 [Objects and Classes in Visual Basic](../Topic/Objects%20and%20Classes%20in%20Visual%20Basic.md)   
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)   
 [Interfaces (Visual Basic)](../vs140/Interfaces--Visual-Basic-.md)