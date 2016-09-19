---
title: "How to: Access a Variable Hidden by a Derived Class (Visual Basic)"
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
ms.assetid: ae21a8ac-9cd4-4fba-a3ec-ecc4321ef93c
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Access a Variable Hidden by a Derived Class (Visual Basic)
When code in a derived class accesses a variable, the compiler normally resolves the reference to the closest accessible version, that is, the accessible version the fewest derivational steps backward from the accessing class. If the variable is defined in the derived class, the code normally accesses that definition.  
  
 If the derived class variable shadows a variable in the base class, it hides the base class version. However, you can access the base class variable by qualifying it with the `MyBase` keyword.  
  
### To access a base class variable hidden by a derived class  
  
-   In an expression or assignment statement, precede the variable name with the `MyBase` keyword and a period (`.`).  
  
     The compiler resolves the reference to the base class version of the variable.  
  
     The following example illustrates shadowing through inheritance. It makes two references, one that accesses the shadowing variable and one that bypasses the shadowing.  
  
    ```  
    Public Class shadowBaseClass  
        Public shadowString As String = "This is the base class string."  
    End Class  
    Public Class shadowDerivedClass  
        Inherits shadowBaseClass  
        Public Shadows shadowString As String = "This is the derived class string."  
        Public Sub showStrings()  
            Dim s As String = "Unqualified shadowString: " & shadowString &  
                vbCrLf & "MyBase.shadowString: " & MyBase.shadowString  
            MsgBox(s)  
        End Sub  
    End Class  
    ```  
  
     The preceding example declares the variable `shadowString` in the base class and shadows it in the derived class. The procedure `showStrings` in the derived class displays the shadowing version of the string when the name `shadowString` is not qualified. It then displays the shadowed version when `shadowString` is qualified with the `MyBase`  keyword.  
  
## Robust Programming  
 To lower the risk of referring to an unintended version of a shadowed variable, you can fully qualify all references to a shadowed variable. Shadowing introduces more than one version of a variable with the same name. When a code statement refers to the variable name, the version to which the compiler resolves the reference depends on factors such as the location of the code statement and the presence of a qualifying string. This can increase the risk of referring to the wrong version of the variable.  
  
## See Also  
 [References to Declared Elements](../vs140/References-to-Declared-Elements--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)   
 [Differences Between Shadowing and Overriding](../vs140/Differences-Between-Shadowing-and-Overriding--Visual-Basic-.md)   
 [How to: Hide a Variable with the Same Name as Your Variable](../vs140/How-to--Hide-a-Variable-with-the-Same-Name-as-Your-Variable--Visual-Basic-.md)   
 [How to: Hide an Inherited Variable](../vs140/How-to--Hide-an-Inherited-Variable--Visual-Basic-.md)   
 [Shadows](../vs140/Shadows--Visual-Basic-.md)   
 [Overrides](../vs140/Overrides--Visual-Basic-.md)   
 [Me, My, MyBase, and MyClass in Visual Basic](../vs140/Me--My--MyBase--and-MyClass-in-Visual-Basic.md)   
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)