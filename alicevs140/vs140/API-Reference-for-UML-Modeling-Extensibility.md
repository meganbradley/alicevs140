---
title: "API Reference for UML Modeling Extensibility"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2b2ffe93-c358-4d28-a5e5-3d0474629b58
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# API Reference for UML Modeling Extensibility
You can write program code to read and modify the models that you create with Visual Studio. The API reference provides information about the specific classes to help you with this. For more task-oriented information, see the topics under [Extending Models and Diagrams](../vs140/Extend-UML-models-and-diagrams.md). To see which versions of Visual Studio support UML models, see [Version support for architecture and modeling tools](../vs140/What-s-new-for-design-in-Visual-Studio.md#VersionSupport).  
  
## Assemblies  
  
|Assembly|What this allows you to do|  
|--------------|--------------------------------|  
|Microsoft.VisualStudio.Uml.Interfaces.dll|-   Read and change model elements such as IUseCase, IAssociation, and so on.<br />-   Navigate relationships between elements.<br /><br /> The namespaces and types correspond to those that are defined in the UML Specification.|  
|Microsoft.VisualStudio.ArchitectureTools.Extensibility.dll|-   Create new instances of model elements<br />-   Access and modify shapes and diagrams.|  
  
## See Also  
 [Extending Models and Diagrams](../vs140/Extend-UML-models-and-diagrams.md)   
 [Visual Studio Modeling SDK API](../Topic/API%20Reference%20for%20Modeling%20SDK%20for%20Visual%20Studio.md)