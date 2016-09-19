---
title: "Object Variable Assignment (Visual Basic)"
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
ms.assetid: 3706811d-fd40-44fe-8727-d692e8e55d6d
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Object Variable Assignment (Visual Basic)
You use a normal assignment statement to assign an object to an object variable. You can assign an object expression or the [Nothing](../Topic/Nothing%20\(Visual%20Basic\).md) keyword, as the following example illustrates.  
  
```  
Dim thisObject As Object  
' The following statement assigns an object reference.  
thisObject = Form1  
' The following statement discontinues association with any object.  
thisObject = Nothing  
```  
  
 `Nothing` means there is no object currently assigned to the variable.  
  
## Initialization  
 When your code begins running, your object variables are initialized to `Nothing`. Those whose declarations include initialization are reinitialized to the values you specify when the declaration statements are executed.  
  
 You can include initialization in your declaration by using the [New](../vs140/New-Operator--Visual-Basic-.md) keyword. The following declaration statements declare object variables `testUri` and `ver` and assign specific objects to them. Each uses one of the overloaded constructors of the appropriate class to initialize the object.  
  
```  
Dim testUri As New System.Uri("http://www.microsoft.com")  
Dim ver As New System.Version(6, 1, 0)  
```  
  
## Disassociation  
 Setting an object variable to `Nothing` discontinues the association of the variable with any specific object. This prevents you from accidentally changing the object by changing the variable. It also allows you to test whether the object variable points to a valid object, as the following example shows.  
  
```  
If otherObject IsNot Nothing Then  
    ' otherObject refers to a valid object, so your code can use it.  
End If  
```  
  
 If the object your variable refers to is in another application, this test cannot determine whether that application has terminated or just invalidated the object.  
  
 An object variable with a value of `Nothing` is also called a *null reference*.  
  
## Current Instance  
 The *current instance* of an object is the one in which the code is currently executing. Since all code executes inside a procedure, the current instance is the one in which the procedure was invoked.  
  
 The `Me` keyword acts as an object variable referring to the current instance. If a procedure is not [Shared (Visual Basic)](../Topic/Shared%20\(Visual%20Basic\).md), it can use the `Me` keyword to obtain a pointer to the current instance. Shared procedures cannot be associated with a specific instance of a class.  
  
 Using `Me` is particularly useful for passing the current instance to a procedure in another module. For example, suppose you have a number of XML documents and wish to add some standard text to all of them. The following example defines a procedure to do this.  
  
```  
Sub addStandardText(XmlDoc As System.Xml.XmlDocument)  
    XmlDoc.CreateTextNode("This text goes into every XML document.")  
End Sub  
```  
  
 Every XML document object could then call the procedure and pass its current instance as an argument. The following example demonstrates this.  
  
```  
addStandardText(Me)  
```  
  
## See Also  
 [Object Variables](../Topic/Object%20Variables%20in%20Visual%20Basic.md)   
 [Object Variable Declaration](../Topic/Object%20Variable%20Declaration%20\(Visual%20Basic\).md)   
 [Object Variable Values](../Topic/Object%20Variable%20Values%20\(Visual%20Basic\).md)   
 [How to: Declare an Object Variable and Assign an Object to It in Visual Basic](../Topic/How%20to:%20Declare%20an%20Object%20Variable%20and%20Assign%20an%20Object%20to%20It%20in%20Visual%20Basic.md)   
 [How to: Make an Object Variable Not Refer to Any Instance](../Topic/How%20to:%20Make%20an%20Object%20Variable%20Not%20Refer%20to%20Any%20Instance%20\(Visual%20Basic\).md)   
 [Me, My, MyBase, and MyClass in Visual Basic](../vs140/Me--My--MyBase--and-MyClass-in-Visual-Basic.md)