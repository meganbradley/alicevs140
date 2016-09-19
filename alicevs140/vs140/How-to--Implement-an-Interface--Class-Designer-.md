---
title: "How to: Implement an Interface (Class Designer)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 81d2cf46-7f60-448c-83e3-1d16bb88ca36
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Implement an Interface (Class Designer)
In Class Designer, you can implement an interface on the class diagram by connecting it to a class that provides code for the interface methods. Class Designer generates an interface implementation and displays the relationship between the interface and the class as an inheritance relationship. You can implement an interface by drawing an inheritance line between the interface and the class or by dragging the interface from Class View.  
  
> [!TIP]
>  You can create interfaces the same way you create other types. If the interface exists but does not appear on the class diagram, then first display it. For more information, see [How to: Create Types on Class Diagrams](../vs140/How-to--Create-Types-by-using-Class-Designer.md) and [How to: View Existing Types](../vs140/How-to--View-Existing-Types--Class-Designer-.md).  
  
### To implement an interface by drawing an inheritance line  
  
1.  On the class diagram, display the interface and the class that will implement the interface.  
  
2.  Draw an inheritance line from the class and the interface.  
  
     A lollipop appears attached to the class and a label with the interface name identifies the inheritance relationship. Visual Studio generates stubs for all interface members.  
  
 For more information, see [How to: Define Inheritance Between Types](../vs140/How-to--Create-Inheritance-Between-Types--Class-Designer-.md).  
  
### To implement an interface from the Class View window  
  
1.  On the class diagram, display the class that you want to implement the interface.  
  
2.  Open Class View and locate the interface.  
  
    > [!TIP]
    >  If Class View is not open, open Class View from the **View** menu. For more information about Class View, see [Viewing Classes and Their Members](assetId:///71e9e8f3-261a-4e0c-87bf-5ec48b8bf333).  
  
3.  Drag the interface node to the class shape on the diagram.  
  
     A lollipop appears attached to the class and a label with the interface name identifies the inheritance relationship. Visual Studio generates stubs for all interface members; at this point, the interface is implemented.  
  
## See Also  
 [How to: Create a Type in a Class Diagram](../vs140/How-to--Create-Types-by-using-Class-Designer.md)   
 [How to: Visualize a Type on the Design Surface](../vs140/How-to--View-Existing-Types--Class-Designer-.md)   
 [How to: Define an Inheritance Relationship](../vs140/How-to--Create-Inheritance-Between-Types--Class-Designer-.md)   
 [Refactoring Classes and Types](../vs140/Refactoring-Classes-and-Types--Class-Designer-.md)