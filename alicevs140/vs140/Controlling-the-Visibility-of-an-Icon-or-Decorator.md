---
title: "Controlling the Visibility of an Icon or Decorator"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2697fd5d-b936-4b6b-b87b-be64825dc7a4
caps.latest.revision: 4
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Controlling the Visibility of an Icon or Decorator
A *decorator* is an icon or line of text that appears on a shape in a domain-specific language (DSL). You can make the decorator appear and disappear depending on the state of properties in the model. For example, on a shape representing a Person, you could have different icons that appear depending on the person's gender, number of children, and so on.  
  
## Controlling the visibility of an icon or decorator  
 The following procedure assumes that you have already defined a shape and its mapping to a domain class. For more information, see [How to Define a Domain Specific Language](../vs140/How-to-Define-a-Domain-Specific-Language.md).  
  
#### To control the visibility of an icon or text decorator  
  
1.  In the DSL Definition diagram, add to the shape class the icons or text decorators that you want to appear.  
  
    1.  Right-click the shape class, point to **Add**, and then click the required type of decorator.  
  
    2.  Set the decorator's **Position** property. More than one decorator can have the same position. For example, you could have icons for male and female sharing the same position.  
  
    3.  Set the **Default Icon** property of an icon decorator.  
  
2.  Select the diagram element map, which is the gray line between the shape class and the domain class on the DSL Definition diagram.  
  
3.  In the DSL Details window, in the **Decorator Maps** tab, select a decorator. For example, the MaleDecorator.  
  
4.  Check the **Visibility Filter** box.  
  
5.  If the domain property that should control visibility is on the immediate domain class, leave **Path to Filter Property** blank.  
  
     Otherwise, click the drop-down menu and navigate to the relationship or class where the property is located.  
  
    -   To avoid an error report, you should not navigate through a relationship marked with "*" in the navigation tool.  
  
6.  Set the **Filter Property** to a domain property. For example, Gender.  
  
7.  In the **Visibility Entries** list, add values of this domain property for which the decorator should be visible. For example, Male.  
  
8.  Repeat the steps for each icon.  
  
9. **Transform All Templates**, build and run, and open a test diagram.  
  
10. When you change the controlling property value, the decorators should appear and disappear.  
  
 Frequently, you want visibility to be controlled by a more complex formula than a simple set of values. For example, to have an icon depend on the number of links of a particular type, or to make it depend on a whether a number is in a particular range. In that case, use the following procedure.  
  
#### To control the visibility of a decorator based on a formula  
  
1.  Add a calculated domain property to the domain class. In the **Properties** window, set the following values:  
  
     **IsBrowsable =**  `False`  **- this hides the property from the user**  
  
     **Kind =**  `Calculated`  **- this means that you will provide code that calculates its value**  
  
     **Name** for example **DecoratorControl**  
  
     **Type** = `Boolean`  
  
     For more information, see [Calculated and Custom Properties](../Topic/Calculated%20and%20Custom%20Storage%20Properties.md).  
  
2.  Make the new property control the decorator visibility.  
  
    1.  Select the diagram element map, which is the gray line from the domain class to the shape. In the **DSL Details** window, open the **DecoratorMap** tab.  
  
    2.  Check the **Visibility Filter** box.  
  
    3.  In **Filter Property**, select the control property **DecoratorControl**.  
  
    4.  Under **Visibility Entries**, enter `True`.  
  
3.  Click **Transform All Templates** in the Solution Explorer toolbar.  
  
4.  Click **Build Solution** on the **Build** menu.  
  
5.  Double-click the error report that has appeared: "*YourClass* does not contain a definition for GetDecoratorControlValue ...".  
  
     The text editor opens on Dsl\GeneratedCode\DomainClasses.cs. Above the highlighted error is a comment that requests you to add a method.  
  
6.  Note the namespace, class and method that are missing.  For example, Company.FamilyTree.Person.GetDecoratorControlValue().  
  
7.  In a separate code file, write a partial class definition that contains the missing method. For example:  
  
    ```  
    namespace Company.FamilyTree  
    { partial class Person  
      { bool GetDecoratorControlValue()  
        {  
          return this.Children.Count > 0;  
    } } }  
    ```  
  
     For more information about customizing the model with program code, see [Navigating and Updating a Model](../Topic/Navigating%20and%20Updating%20a%20Model%20in%20Program%20Code.md).  
  
8.  Rebuild and run the solution.  
  
## See Also  
 [How to Display Shapes with Image and Text Fields](../vs140/Defining-Shapes-and-Connectors.md)   
 [Setting a Background Image on a Diagram](../vs140/Setting-a-Background-Image-on-a-Diagram.md)   
 [Navigating and Updating a Model](../Topic/Navigating%20and%20Updating%20a%20Model%20in%20Program%20Code.md)   
 [Writing Code to Customize a Domain-Specific Language](../vs140/Writing-Code-to-Customise-a-Domain-Specific-Language.md)