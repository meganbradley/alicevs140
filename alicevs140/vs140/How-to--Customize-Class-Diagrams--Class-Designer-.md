---
title: "How to: Customize Class Diagrams (Class Designer)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9030aea-c77d-4cc1-b8f6-b6ca469b692d
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Customize Class Diagrams (Class Designer)
You can change the way that class diagrams display information. You can customize the whole diagram or the individual types on the design surface.  
  
 For example, you can adjust the zoom level of an entire class diagram, change how individual type members are grouped and sorted, hide or show relationships, and move individual or sets of types anywhere on the diagram.  
  
> [!NOTE]
>  Customizing the way that shapes appear on the diagram doesn't change the underlying code for the types represented on the diagram.  
  
 The sections that contain type members, such as the Properties section in a class, are called compartments. You can hide or show individual compartments and type members.  
  
 **In this topic**  
  
-   [Zoom in and out of the class diagram](../vs140/How-to--Customize-Class-Diagrams--Class-Designer-.md#ZoomInOut)  
  
-   [Customize grouping and sorting of type members](../vs140/How-to--Customize-Class-Diagrams--Class-Designer-.md#CustomizeGroupingSorting)  
  
-   [Hide compartments on a type](../vs140/How-to--Customize-Class-Diagrams--Class-Designer-.md#HideCompartments)  
  
-   [Hide individual members on a type](../vs140/How-to--Customize-Class-Diagrams--Class-Designer-.md#HideMembers)  
  
-   [Show hidden compartments and members on a type](../vs140/How-to--Customize-Class-Diagrams--Class-Designer-.md#DisplayHiddenCompartmentsAndMemberrs)  
  
-   [Hide relationships](../vs140/How-to--Customize-Class-Diagrams--Class-Designer-.md#HideAssociationAndInheritance)  
  
-   [Show hidden relationhips](../vs140/How-to--Customize-Class-Diagrams--Class-Designer-.md#DisplayAssociationAndInheritance)  
  
-   [Remove a type shape from a class diagram](../vs140/How-to--Customize-Class-Diagrams--Class-Designer-.md#RemoveCodeAndShape)  
  
-   [Delete a type shape and its underlying code](../vs140/How-to--Customize-Class-Diagrams--Class-Designer-.md#DeleteTypeShapeAndCode)  
  
##  <a name="ZoomInOut"></a> Zoom in and out of the class diagram  
  
1.  Open and select a class diagram file in Class Designer.  
  
2.  On the Class Designer toolbar, click the **Zoom In** or **Zoom Out** button to change the zoom level of the designer surface.  
  
     or  
  
     Specify a particular zoom value. You can use the **Zoom** drop down list or type a valid zoom level (valid range is between 10% and 400%).  
  
    > [!NOTE]
    >  Changing the zoom level does not affect the scale of your class diagram printout.  
  
##  <a name="CustomizeGroupingSorting"></a> Customize grouping and sorting of type members  
  
1.  Open and select a class diagram file in Class Designer.  
  
2.  Right-click an empty area on the design surface and point to **Group Members**.  
  
3.  Select one of the available options:  
  
    1.  **Group by Kind** separates individual type members into a grouped list of Properties, Methods, Events, and Fields. The individual groups depend on the entities definition: for example, a class will not display any events group if there are no events yet defined for that class.  
  
    2.  **Group by Access** separates individual type members into a grouped list based on the member's access modifiers. For example, Public and Private.  
  
    3.  **Sort Alphabetically** displays the items that make up an entity as a single alphabetized list. The list is sorted in ascending order.  
  
##  <a name="HideCompartments"></a> Hide compartments on a type  
  
1.  Open and select a class diagram file in the class designer.  
  
2.  Right click the member category in the type you want to customize (for example, select the **Methods** node in a class.  
  
3.  Click **Hide Compartment**.  
  
     The selected compartment disappears from the type container.  
  
##  <a name="HideMembers"></a> Hide individual members on a type  
  
1.  Open and select a class diagram file in Class Designer.  
  
2.  Right-click the member in the type you want to hide.  
  
3.  Click **Hide**.  
  
     The selected member disappears from the type container.  
  
##  <a name="DisplayHiddenCompartmentsAndMemberrs"></a> Show hidden compartments and members on a type  
  
1.  Open and select a class diagram file in Class Designer.  
  
2.  Right-click the name of the type with the hidden compartment.  
  
3.  Click **Show All Members**.  
  
     All hidden compartments and members appear in the type container.  
  
##  <a name="HideAssociationAndInheritance"></a> Hide relationships  
  
1.  Open and select a class diagram file in Class Designer.  
  
2.  Right-click the association or inheritance line that you want to hide.  
  
3.  Click **Hide** for association lines, and click **Hide Inheritance Line** for inheritance lines.  
  
4.  Click **Show All Members**.  
  
     All hidden compartments and members appear in the type container.  
  
##  <a name="DisplayAssociationAndInheritance"></a> Show hidden relationships  
  
1.  Open and select a class diagram file in Class Designer.  
  
2.  Right-click the type with the hidden association or inheritance.  
  
 Click **Show All Members** for association lines, and click **Show Base Class** or **Show Derived Classes** for inheritance lines.  
  
##  <a name="RemoveCodeAndShape"></a> Remove a shape from a class diagram  
 You can remove a type shape from the class diagram without affecting the type's underlying code. Removing type shapes from a class diagram affects only that diagram: the underlying code that defines the type and other diagrams that display the type are not affected.  
  
1.  On the class diagram, select the type shape you want to remove from the diagram.  
  
2.  On the **Edit** menu, choose **Remove from Diagram**.  
  
     The type shape and any lines of association or inheritance connected to the shape no longer appear on the diagram.  
  
##  <a name="DeleteTypeShapeAndCode"></a> Delete a type shape and its underlying code  
  
1.  Right-click the shape on the design surface.  
  
2.  Select **Delete Code** from the context menu.  
  
     The shape is removed from the diagram and its underlying code is deleted from the project.  
  
## See Also  
 [Working with Class Diagrams](../vs140/Working-with-Class-Diagrams--Class-Designer-.md)   
 [How to: Change Between Member Notation and Association Notation](../vs140/How-to--Change-Between-Member-Notation-and-Association-Notation--Class-Designer-.md)   
 [How to: View Existing Types on Class Diagrams](../vs140/How-to--View-Existing-Types--Class-Designer-.md)   
 [Viewing Types and Relationships on Class Diagrams](../vs140/Viewing-Types-and-Relationships--Class-Designer-.md)