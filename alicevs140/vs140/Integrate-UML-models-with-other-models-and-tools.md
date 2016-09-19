---
title: "Integrate UML models with other models and tools"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9e75e7d1-93cf-4196-baa3-bd10b9af16d3
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Integrate UML models with other models and tools
UML models can be integrated with other models and with domain-specific languages.  
  
 You can integrate models in the following ways by writing extension code to perform a variety of functions:  
  
 Attach references from any element to other items such as files or to elements in other models.  
 In a UML element, you can store links to other UML elements, files, or other objects by encoding their identities as strings.  
  
 For example, you could write an extension that can link any UML action (that is, an element in an activity diagram) to another activity diagram. When the user double-clicks the action, the other diagram opens. This lets the user provide a more detailed view of the action.  
  
 There are two ways in which you can store strings and other data in any element:  
  
-   **Stereotype properties.** You can define a UML profile, in which you define a stereotype that adds properties to specified kinds of UML element. For example, you could define a profile that adds a property named **MoreDetail** to a UML action. You could write extension code that stores link data in an action by applying the stereotype to the action, and then storing the data in the property.  
  
     The stereotype and its properties are visible to the user in the Properties window.  
  
     To deploy this extension, you would package the profile definition and the extension code in a single [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Extension.  
  
     For more information, see [How to Define Profiles](../vs140/Define-a-profile-to-extend-UML.md).  
  
     For a sample project in which a profile is deployed together with menu commands and gesture handlers, see [Sample: UML Profiles](http://go.microsoft.com/fwlink/?LinkID=213811).  
  
-   **References.** You can attach a set of strings to any UML element. You could write code that stores the information such as a filename or the GUID of another element. This can be done without providing additional definitions. References are not directly visible to the user.  
  
     For more information, see [How to associate References](../vs140/Attach-reference-strings-to-UML-model-elements.md). For a sample, see [Link UML Elements to Diagrams or other Files](http://go.microsoft.com/fwlink/?LinkId=213813).  
  
 There are two ways to encode references to model elements:  
  
-   **GUID and Filename** of the target model element and the model that contains it, or a particular diagram that displays it.  
  
     For an example, see [Link UML Elements to Diagrams or other Files](http://go.microsoft.com/fwlink/?LinkId=213813).  
  
-   **ModelBus References.** ModelBus is a framework for creating and resolving references between models. It includes the ModelBus Picker, which lets the user select an element in a model. It also helps the user to resolve references that are lost because of changes in the target model.  
  
     For more information, see [Integrating Models](../Topic/Integrating%20Models%20by%20using%20Visual%20Studio%20Modelbus.md).  
  
 Propagate changes from one model to another.  
 For example, you could synchronize the name of an element with the name of the linked diagram, so that if the user changes one, the other also changes. There are two mechanisms for doing this:  
  
1.  **VMSDK Rules** can be used to propagate changes inside the same model.  
  
     For an example, see [Link UML Elements to Diagrams or other Files](http://go.microsoft.com/fwlink/?LinkId=213813).  
  
2.  **VMSDK Events** can be used to propagate changes outside the model – for example, to change the filename of a linked document, or to change an element in another model.  
  
 For information about both these mechanisms, see [How to respond to changes in UML](../vs140/How-to--Respond-to-Changes-in-a-UML-Model.md).  
  
 Drag elements to copy them from one model to another  
 You can let the user create elements by dragging items onto a UML diagram. The created element does not have to be a copy of the original. For example, you could let the user drag an activity diagram from solution explorer onto another activity diagram, to create a new action.  
  
 For more information see [How to Define a Gesture Handler](../Topic/Define%20a%20gesture%20handler%20on%20a%20modeling%20diagram.md) and [How to Write a Drag and Drop Handler](../Topic/How%20to:%20Add%20a%20Drag-and-Drop%20Handler.md).  
  
## Samples  
 Please see the code sample [Link UML Elements to Diagrams or other Files](http://go.microsoft.com/fwlink/?LinkId=213813). The sample lets users drag a file onto any UML element, and later open the file by double-clicking the element. For example, you could link an activity diagram to a use case element. An icon shows which elements have links.  
  
 This code sample demonstrates the following techniques:  
  
-   [How to associate References](../vs140/Attach-reference-strings-to-UML-model-elements.md)  
  
     The sample code stores file paths and element GUIDs in reference strings that are associated with the element.  
  
-   How to add decorators to UML elements. For general information about decorators, see [Customizing Image and Text Fields](../vs140/Customizing-Text-and-Image-Fields.md).  
  
     The sample adds an image decorator to the UML shapes.  
  
-   [How to Respond to Changes in a UML Model](../vs140/How-to--Respond-to-Changes-in-a-UML-Model.md)  
  
     The sample demonstrates how to define a rule that responds to new shapes appearing on a diagram.  
  
-   [How to Define a Menu Command](../Topic/Define%20a%20menu%20command%20on%20a%20modeling%20diagram.md)  
  
-   [How to Define a Gesture Handler](../Topic/Define%20a%20gesture%20handler%20on%20a%20modeling%20diagram.md)  
  
     The sample demonstrates how to handle items dragged from Windows Explorer (or File Explorer), Solution Explorer, and other UML elements.  
  
 For an example in which a UML model is be read by a DSL, see [How to Write a Drag and Drop Handler](../Topic/How%20to:%20Add%20a%20Drag-and-Drop%20Handler.md).  
  
## See Also  
 [How to Define a Menu Command](../Topic/Define%20a%20menu%20command%20on%20a%20modeling%20diagram.md)   
 [How to Define a Gesture Handler](../Topic/Define%20a%20gesture%20handler%20on%20a%20modeling%20diagram.md)   
 [How to Write a Drag and Drop Handler](../Topic/How%20to:%20Add%20a%20Drag-and-Drop%20Handler.md)   
 [How to Respond to Changes in a UML Model](../vs140/How-to--Respond-to-Changes-in-a-UML-Model.md)   
 [Sample: UML Profiles](http://go.microsoft.com/fwlink/?LinkID=213811)   
 [Link UML Elements to Diagrams or other Files](http://go.microsoft.com/fwlink/?LinkId=213813)