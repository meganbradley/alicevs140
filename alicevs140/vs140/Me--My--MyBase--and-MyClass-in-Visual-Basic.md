---
title: "Me, My, MyBase, and MyClass in Visual Basic"
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
ms.assetid: f8e241ae-b1ed-4886-9aa0-08c632154029
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Me, My, MyBase, and MyClass in Visual Basic
`Me`, `My`, `MyBase`, and `MyClass` in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] have similar names, but different purposes. This topic describes each of these entities in order to distinguish them.  
  
## Me  
 The `Me` keyword provides a way to refer to the specific instance of a class or structure in which the code is currently executing. `Me` behaves like either an object variable or a structure variable referring to the current instance. Using `Me` is particularly useful for passing information about the currently executing instance of a class or structure to a procedure in another class, structure, or module.  
  
 For example, suppose you have the following procedure in a module.  
  
```  
Sub ChangeFormColor(FormName As Form)  
   Randomize()  
   FormName.BackColor = Color.FromArgb(Rnd() * 256, Rnd() * 256, Rnd() * 256)  
End Sub  
```  
  
 You can call this procedure and pass the current instance of the <xref:System.Windows.Forms.Form?qualifyHint=False> class as an argument by using the following statement.  
  
```  
ChangeFormColor(Me)  
```  
  
## My  
 The `My` feature provides easy and intuitive access to a number of [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] classes, enabling the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] user to interact with the computer, application, settings, resources, and so on.  
  
## MyBase  
 The `MyBase` keyword behaves like an object variable referring to the base class of the current instance of a class. `MyBase` is commonly used to access base class members that are overridden or shadowed in a derived class. `MyBase.New` is used to explicitly call a base class constructor from a derived class constructor.  
  
## MyClass  
 The `MyClass` keyword behaves like an object variable referring to the current instance of a class as originally implemented. `MyClass` is similar to `Me`, but all method calls on it are treated as if the method were `NotOverridable`.  
  
## See Also  
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)