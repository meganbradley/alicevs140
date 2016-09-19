---
title: "References and the Imports Statement (Visual Basic)"
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
ms.assetid: 38149bd4-0a6f-4b31-b5f8-94a8c33f1600
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# References and the Imports Statement (Visual Basic)
You can make external objects available to your project by choosing the **Add Reference** command on the **Project** menu. References in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] can point to assemblies, which are like type libraries but contain more information.  
  
## The Imports Statement  
 Assemblies include one or more namespaces. When you add a reference to an assembly, you can also add an `Imports` statement to a module that controls the visibility of that assembly's namespaces within the module. The `Imports` statement provides a scoping context that lets you use only the portion of the namespace necessary to supply a unique reference.  
  
 The `Imports` statement has the following syntax:  
  
 `Imports` [`|``Aliasname` =] `Namespace`  
  
 `Aliasname` refers to a short name you can use within code to refer to an imported namespace. `Namespace` is a namespace available through either a project reference, through a definition within the project, or through a previous `Imports` statement.  
  
 A module may contain any number of `Imports` statements. They must appear after any `Option` statements, if present, but before any other code.  
  
> [!NOTE]
>  Do not confuse project references with the `Imports` statement or the `Declare` statement. Project references make external objects, such as objects in assemblies, available to [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] projects. The `Imports` statement is used to simplify access to project references, but does not provide access to these objects. The `Declare` statement is used to declare a reference to an external procedure in a dynamic-link library (DLL).  
  
## Using Aliases with the Imports Statement  
 The `Imports` statement makes it easier to access methods of classes by eliminating the need to explicitly type the fully qualified names of references. Aliases let you assign a friendlier name to just one part of a namespace. For example, the carriage return/line feed sequence that causes a single piece of text to be displayed on multiple lines is part of the <xref:Microsoft.VisualBasic.ControlChars?qualifyHint=False> module in the <xref:Microsoft.VisualBasic?qualifyHint=True> namespace. To use this constant in a program without an alias, you would need to type the following code:  
  
 [!CODE [VbVbalrApplication#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrApplication#3)]  
  
 `Imports` statements must always be the first lines immediately following any `Option` statements in a module. The following code fragment shows how to import and assign an alias to the <xref:Microsoft.VisualBasic.ControlChars?qualifyHint=True> module:  
  
 [!CODE [VbVbalrApplication#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrApplication#4)]  
  
 Future references to this namespace can be considerably shorter:  
  
 [!CODE [VbVbalrApplication#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrApplication#5)]  
  
 If an `Imports` statement does not include an alias name, elements defined within the imported namespace can be used in the module without qualification. If the alias name is specified, it must be used as a qualifier for names contained within that namespace.  
  
## See Also  
 <xref:Microsoft.VisualBasic.ControlChars?qualifyHint=False>   
 <xref:Microsoft.VisualBasic?qualifyHint=False>   
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](assetId:///3bd75d61-f00c-47c0-86a2-dd1f20e231c9)   
 [Namespaces in Visual Basic](../Topic/Namespaces%20in%20Visual%20Basic.md)   
 [Assemblies and the Global Assembly Cache (C# and Visual Basic)](../vs140/Assemblies-and-the-Global-Assembly-Cache--C#-and-Visual-Basic-.md)   
 [How to: Create and Use DLLs (C# and Visual Basic)](../vs140/How-to--Create-and-Use-Assemblies-Using-the-Command-Line--C#-and-Visual-Basic-.md)   
 [Imports Statement (.NET Namespace and Type)](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md)