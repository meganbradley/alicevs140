---
title: "Get UML model elements from IDataObject"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e0b9cec8-3b93-4a24-8bd3-3e086501d387
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Get UML model elements from IDataObject
When the user drags elements from any source onto a diagram, the dragged elements are encoded in a `System.Windows.Forms.IDataObject`. The encoding depends on the type of source object. The following fragment demonstrates how to retrieve the elements when the source is a UML diagram.  
  
> [!NOTE]
>  Most of the operations that you have to do on UML models can be performed by using the types in defined in the assemblies **Microsoft.VisualStudio.Uml.Interfaces** and **Microsoft.VisualStudio.ArchitectureTools.Extensibility**. But for this purpose, you have to use some classes that are part of the implementation of the UML modeling tools. For example, `ShapeElement` in this fragment is not the same as the UML `IShape`. To reduce the risk of putting the UML model and diagrams into an inconsistent state, it is better to avoid using the methods on these implementation classes, except where there is no alternative.  
  
## Code Sample  
 Your project must reference the following [!INCLUDE[TLA2#tla_net](../vs140/includes/TLA2#tla_net_md.md)] assemblies:  
  
 **Microsoft.VisualStudio.Modeling.Sdk.[version]**  
  
 **Microsoft.VisualStudio.Modeling.Sdk.Diagrams.[version]**  
  
 **System.Windows.Forms**  
  
```  
using Microsoft.VisualStudio.Modeling;    
  // for ElementGroupPrototype  
using Microsoft.VisualStudio.Modeling.Diagrams;    
  // for ShapeElement, DiagramDragEventArgs, DiagramPointEventArgs  
…   
  /// <summary>  
  /// Retrieves UML IElements from drag arguments.  
  /// Works for drags from UML diagrams.  
  /// </summary>  
  private IEnumerable<IElement> GetModelElementsFromDragEvent  
                  (DiagramDragEventArgs dragEvent)  
  {  
     //ElementGroupPrototype is the container for  
     //dragged and copied elements and toolbox items.  
     ElementGroupPrototype prototype =  
        dragEvent.Data.  
        GetData(typeof(ElementGroupPrototype))  
                     as ElementGroupPrototype;  
     // Locate the originals in the implementation store.  
     IElementDirectory implementationDirectory =   
        dragEvent.DiagramClientView.Diagram.Store.ElementDirectory;  
  
     return  prototype.ProtoElements.Select(  
       prototypeElement =>   
       {  
          ModelElement element = implementationDirectory  
                .FindElement(prototypeElement.ElementId);  
          ShapeElement shapeElement = element as ShapeElement;  
          if (shapeElement != null)  
          {   
            // Dragged from a diagram.  
            return shapeElement.ModelElement as IElement;  
          }  
          else  
          {   
            // Dragged from UML Model Explorer.  
            return element as IElement;  
          }  
        });  
    }  
```  
  
 For more information about `ElementGroupPrototype` and the `Store` in which the UML modeling tools are implemented, see [Domain-Specific Languages](../vs140/Modeling-SDK-for-Visual-Studio---Domain-Specific-Languages.md).  
  
## See Also  
 [Programming with the UML API](../Topic/Programming%20with%20the%20UML%20API.md)   
 [How to: Define a Gesture Handler on a UML Diagram](../Topic/Define%20a%20menu%20command%20on%20a%20modeling%20diagram.md)