---
title: "How to: Create Associations Between Types (Class Designer)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: adccb9c8-2f8a-4086-9fa9-f70f99fb6e00
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create Associations Between Types (Class Designer)
Association lines in Class Designer show how classes in a diagram are related. An Association line represents a class that is the type of a property or field of another class in your project. Association lines are generally used to illustrate the most important relationships between classes in your project.  
  
 While you could display all fields and properties as associations, it makes more sense to show only important members as associations, depending on what you intend to emphasize in the diagram. (You can show less important members as regular members or hide them altogether.)  
  
> [!NOTE]
>  Class Designer supports only unidirectional associations.  
  
### To define an association line in the Class Diagram  
  
1.  In the Toolbox, under Class Designer, select **Association**.  
  
2.  Draw a line between the two shapes you want to link with an association.  
  
     A new property is created in the first class. This property displays as an association line (not as a property within a compartment in the shape) with a default name. Its type is the shape to which the association line points.  
  
### To change the name of an association  
  
-   On the diagram surface, click the label of the association line and edit it.  
  
 \- or -  
  
1.  Click the shape that contains the property that is shown as an association.  
  
     The shape obtains focus and its members display in the Class Details window and in the Properties window.  
  
2.  In either the Class Details window or the Properties window, edit the name field for that property and press Enter.  
  
     The name is updated in the **Class Details** window, on the association line, in the Properties window, and in code.  
  
## See Also  
 [How to: Change Between Member Notation and Association Notation](../vs140/How-to--Change-Between-Member-Notation-and-Association-Notation--Class-Designer-.md)