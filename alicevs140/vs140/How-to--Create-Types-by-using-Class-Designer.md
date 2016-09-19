---
title: "How to: Create Types by using Class Designer"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 94458c31-28bc-40e2-9737-85868788a0e5
caps.latest.revision: 43
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create Types by using Class Designer
To design new types for Visual C# .NET and Visual Basic .NET projects, create them on a class diagram. To see existing types, see [How to: View Existing Types](../vs140/How-to--View-Existing-Types--Class-Designer-.md).  
  
-   [Create a new type](#CreateType)  
  
-   [Apply a custom attribute to a type](#CustAttributeType)  
  
-   [Apply a custom attribute to a type member](#CustAttributeMember)  
  
##  <a name="CreateType"></a> Create a new type  
  
1.  In the Toolbox, under Class Designer, drag one of these onto a class diagram:  
  
    -   **Class** or **Abstract Class**  
  
    -   **Enum**  
  
    -   **Interface**  
  
    -   **Structure** (VB) or **Struct** (C#)  
  
    -   **Delegate**  
  
    -   **Module** (VB only)  
  
2.  Name the type. Then select its access level.  
  
3.  Select the file where you want to add the initial code for the type:  
  
    -   To create a new file and add it to the current project, select **Create new file** and name the file.  
  
    -   To add code to an existing file, select **Add to existing file**.  
  
         If your solution has a project that shares code across multiple apps, you can add a new type to a class diagram in the app project, but only if the corresponding class file is in the same app project or is in the shared project.  
  
4.  Now add other items to define the type:  
  
    |||  
    |-|-|  
    |**For**|**Add**|  
    |Classes, abstract classes, structures or structs|Methods, properties, fields, events, constructors (method), destructors (method), and constants that define the type|  
    |Enums|Field values that make up the enumeration|  
    |Interfaces|Methods, properties, and events that make up the interface|  
    |Delegate|Parameters that define the delegate|  
    |Module|Methods, properties, fields, events, constructors (method), and constants that define the module|  
  
     See [Creating Members](../vs140/Creating-and-Configuring-Type-Members--Class-Designer-.md#CreateMembers).  
  
##  <a name="CustAttributeType"></a> Apply a custom attribute to a type  
  
1.  Click the type's shape on a class diagram.  
  
2.  In the Properties window, next to the **Custom Attributes** property for the type, click the ellipsis (…) button.  
  
3.  Add one or more custom attributes with one per line. Don't enclose them in brackets.  
  
     When you're done, the custom attributes are applied to the type.  
  
##  <a name="CustAttributeMember"></a> Apply a custom attribute to a type member  
  
1.  Click the member's name in its type's shape on a class diagram, or its row in the Class Details window.  
  
2.  In the Properties window, find the member's **Custom Attributes** property.  
  
3.  Add one or more custom attributes with one per line. Don't enclose them in brackets.  
  
     When you're done, the custom attributes are applied to the type.  
  
## See Also  
 [How to: Define Inheritance Between Types](../vs140/How-to--Create-Inheritance-Between-Types--Class-Designer-.md)   
 [How to: Define Associations Between Types](../vs140/How-to--Create-Associations-Between-Types--Class-Designer-.md)   
 [Creating and Configuring Type Members](../vs140/Creating-and-Configuring-Type-Members--Class-Designer-.md)   
 [Working with Class Diagrams](../vs140/Working-with-Class-Diagrams--Class-Designer-.md)   
 [Designing Classes and Types](../vs140/Designing-Classes-and-Types--Class-Designer-.md)