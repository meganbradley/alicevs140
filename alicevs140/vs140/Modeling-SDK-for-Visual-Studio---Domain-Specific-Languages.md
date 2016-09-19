---
title: "Modeling SDK for Visual Studio - Domain-Specific Languages"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-techdebt
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 17a531e2-1964-4a9d-84fd-6fb1b4aee662
caps.latest.revision: 79
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Modeling SDK for Visual Studio - Domain-Specific Languages
By using the Modeling SDK for [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] (MSDK), you can create powerful model-based development tools that you can integrate into [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. As an example, the UML tools are created using MSDK. In the same manner, you can create one or more model definitions and integrate them into a set of tools.  
  
 At the heart of MSDK is the definition of a model that you create to represent concepts in your business area. You can surround the model with a variety of tools, such as a diagrammatic view, the ability to generate code and other artifacts, commands for transforming the model, and the ability to interact with code and other objects in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. As you develop the model, you can combine it with other models and tools to form a powerful toolset that is centered on your development.  
  
 MSDK lets you develop a model quickly in the form of a domain-specific language (DSL). You begin by using a specialized editor to define a schema or abstract syntax together with a graphical notation. From this definition, VMSDK generates:  
  
-   A model implementation with a strongly-typed API that runs in a transaction-based store.  
  
-   A tree-based explorer.  
  
-   A graphical editor in which users can view the model or parts of it that you define.  
  
-   Serialization methods that save your models in readable XML.  
  
-   Facilities for generating program code and other artifacts using text templating.  
  
 You can customize and extend all of these features. Your extensions are integrated in such a way that you can still update the DSL definition and re-generate the features without losing your extensions.  
  
## Samples and the Latest Information  
 [Download the Modeling SDK for Visual Studio 2015](http://www.microsoft.com/download/details.aspx?id=48148)  
  
 [Samples](http://go.microsoft.com/fwlink/?LinkId=186128) for the Modeling SDK for Visual Studio.  
  
 For guidance on advanced techniques and troubleshooting, visit [Visual Studio DSL & Modeling Tools Extensibility forum](http://go.microsoft.com/fwlink/?LinkID=186074).  
  
## In This Section  
 [Getting Started with Domain-Specific Languages](../vs140/Getting-Started-with-Domain-Specific-Languages.md)  
  
 [Understanding Models, Classes and Relationships](../vs140/Understanding-Models--Classes-and-Relationships.md)  
  
 [How to Define a Domain-Specific Language](../vs140/How-to-Define-a-Domain-Specific-Language.md)  
  
 [Customizing Domain-Specific Languages](../Topic/Customizing%20and%20Extending%20a%20Domain-Specific%20Language.md)  
  
 [Adding Validation to DSLs](../Topic/Validation%20in%20a%20Domain-Specific%20Language.md)  
  
 [Programming Domain-Specific Languages](../vs140/Writing-Code-to-Customise-a-Domain-Specific-Language.md)  
  
 [Generating Code in DSLs](../vs140/Generating-Code-from-a-Domain-Specific-Language.md)  
  
 [Understanding the Generated Code](../Topic/Understanding%20the%20DSL%20Code.md)  
  
 [Customizing Serialization Behavior](../vs140/Customizing-File-Storage-and-XML-Serialization.md)  
  
 [Deploying DSLs](../vs140/Deploying-Domain-Specific-Language-Solutions.md)  
  
 [Creating a Windows Forms-based DSL](../Topic/Creating%20a%20Windows%20Forms-Based%20Domain-Specific%20Language.md)  
  
 [Creating a WPF-based DSL](../vs140/Creating-a-WPF-Based-Domain-Specific-Language.md)  
  
 [Customizing the DSL Designer](../vs140/How-to--Extend-the-Domain-Specific-Language-Designer.md)  
  
 [Supported VS Editions](../vs140/Supported-Visual-Studio-Editions-for-Visualization---Modeling-SDK.md)  
  
 [How to Migrate](../vs140/How-to--Migrate-a-Domain-Specific-Language-to-a-New-Version.md)  
  
 [API Reference for VSVSMSDK](../Topic/API%20Reference%20for%20Modeling%20SDK%20for%20Visual%20Studio.md)