---
title: "Refactoring Classes and Types (Class Designer)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dcf07bb4-fa3b-4224-9dec-566fd924a8ce
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Refactoring Classes and Types (Class Designer)
When you refactor code, you make it easier to understand, maintain, and more efficient by changing its internal structure and how its objects are designed, not its external behavior. Use Class Designer and the Class Details window to reduce the work that you have to do and the chance of introducing bugs when you refactor Visual C# .NET, Visual Basic .NET, or C++ code in your Visual Studio project.  
  
> [!NOTE]
>  The files of a project might be read-only because the project is under source-code control and is not checked out; it is a referenced project; or its files are marked as read-only on disk. When you work in a project in one of these states, you will be presented with various ways to save your work depending on the project’s state. This applies to refactoring code and also to code that you change in another way, such as directly editing it. For more information, see [Display of Read-Only Information (Class Designer)](assetId:///33e2d3a9-1668-4d10-ae56-fa09b3156e0a).  
  
## Common Tasks  
  
|Task|Supporting Content|  
|----------|------------------------|  
|**Refactoring classes:** You can use refactoring operations to split a class into partial classes or to implement an abstract base class.|-   [How to: Split a Class into Partial Classes (Class Designer)](../vs140/How-to--Split-a-Class-into-Partial-Classes--Class-Designer-.md)|  
|**Working with interfaces:** In Class Designer, you can implement an interface on the class diagram by connecting it to a class that provides code for the interface methods.|-   [How to: Implement an Interface (Class Designer)](../vs140/How-to--Implement-an-Interface--Class-Designer-.md)|  
|**Refactoring types, type members, and parameters:** By using Class Designer, you can rename types, override type members, or move them from one type to another. You can also create nullable types.|-   [Renaming Types and Type Members](../vs140/Refactoring-Classes-and-Types--Class-Designer-.md#RenamingTypesAndMembers)<br />-   [Moving Type Members from One Type to Another](../vs140/Refactoring-Classes-and-Types--Class-Designer-.md#MovingTypeMembers)<br />-   [How to: Create a Nullable Type (Class Designer)](../Topic/How%20to:%20Create%20a%20Nullable%20Type%20\(Class%20Designer\).md)|  
  
###  <a name="RenamingTypesAndMembers"></a> Renaming Types and Type Members  
 In Class Designer, you can rename a type or a member of a type on the class diagram or in the Properties window. In the Class Details window, you can change the name of a member but not a type. Renaming a type or type member propagates to all windows and code locations where the old name appeared.  
  
##### To rename a name in the Class Designer  
  
1.  On the class diagram, select the type or member and click on the name.  
  
     The name of the member becomes editable.  
  
2.  Type the new name for the type or type member  
  
##### To rename a name in the Class Details Window  
  
1.  To display the Class Details window, right-click the type or type member and then click **Class Details**.  
  
     The Class Details window appears.  
  
2.  In the **Name** column, change the name of the type member  
  
3.  To move focus away from the cell, press the **ENTER** key or click away from the cell.  
  
    > [!NOTE]
    >  In the Class Details window, you can change the name of a member but not a type.  
  
##### To rename a name in the Properties window  
  
1.  On the class diagram or the Class Details window, right-click the type or member and then click **Properties**.  
  
     The Properties window appears and displays properties for the type or type member.  
  
2.  In the **Name** property, change the name of the type or type member.  
  
     The new name propagates to all windows and code locations in the current project where the old name appeared.  
  
###  <a name="MovingTypeMembers"></a> Moving Type Members from One Type to Another  
 Using **Class Designer**, you can move a type member from one type to another type, if both are visible in the current class diagram.  
  
##### To move a type member from one type to another  
  
1.  In a type that is visible on the design surface, right-click the member you want to move to another type, and then click **Cut**.  
  
2.  Right-click the destination type and then click **Paste**.  
  
     The property is removed from the source type and appears in the destination type.  
  
## Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[Visualize Existing Classes, Types, and Relationships in a Diagram](../vs140/Viewing-Types-and-Relationships--Class-Designer-.md)||  
|[Design Classes and Types](../vs140/Designing-Classes-and-Types--Class-Designer-.md)||