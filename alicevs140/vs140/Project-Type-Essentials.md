---
title: "Project Type Essentials"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 09991589-2300-430e-b6a4-7f2b95fe676f
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Project Type Essentials
[!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] includes several project types for languages such as [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] or [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]. [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] also lets you create your own project types.  
  
 If you just want to add custom commands, editors, or tool windows to [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], you can do so without creating a new project type. For more information, see the following topics:  
  
-   [Menu and Toolbar Commands](../Topic/Commands,%20Menus,%20and%20Toolbars.md)  
  
-   [Editors](../vs140/Editor-and-Language-Service-Extensions.md)  
  
-   [Extending and Customizing Tool Windows](../Topic/Extending%20and%20Customizing%20Tool%20Windows.md)  
  
 Likewise, if you want to customize the behavior of the supplied [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] and [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] project types, you can do so using project subtypes. For more information, see [Project Subtypes](../Topic/Project%20Subtypes.md).  
  
 You must create a new project type for projects that are based on a language other than [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] and [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] if you want to support one or more of the following:  
  
-   Build  
  
-   Deployment  
  
-   Multiple configurations  
  
-   Source control  
  
-   Debugging  
  
-   Project items in Solution Explorer  
  
-   The **Open Project** or **New Project** dialog boxes  
  
-   Project nesting  
  
-   For more information about the capabilities of project types, see the following:  
  
-   Project types are objects in a VSPackage that implement the set of interfaces [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] expects. If you are using C# to develop a project type, the Managed Package Framework project classes implement the necessary interfaces for you and let you inherit that implementation. For more information, see [Using MPF Project Classes to Implement a Project Type (C#)](../vs140/Using-the-Managed-Package-Framework-to-Implement-a-Project-Type--C#-.md).  
  
-   For C++ developers, the classes in the HierUtil library work in a similar manner. For more information, see [Not in Build: Using HierUtil7 Project Classes to Implement a Project Type (C++)](assetId:///a5c16a09-94a2-46ef-87b5-35b815e2f346).  
  
-   Project types can support data other than typical source code files that build into an .exe or .dll assembly. For example, [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] database projects contain references to script and query files stored on disk and add commands to **Solution Explorer** to execute the scripts and queries against a database, but the projects do not support build behavior. For more information, see [Opening and Saving Project Items](../vs140/Opening-and-Saving-Project-Items.md).  
  
-   A project type does not have to use files at all. For example, a project type could store all its data in a database. [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] gives project types complete control over how they persist data for projects and project items. For more information, see [Project Type Design Decisions](../vs140/Project-Type-Design-Decisions.md).  
  
-   Project types must provide a *project factory*, which is an object that creates an instance of the project type whenever [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] is told to open or create a project that is based on that project type. For more information, see [Creating Project Instances with Project Factories](../vs140/Creating-Project-Instances-By-Using-Project-Factories.md).  
  
-   Project types must supply templates for projects and project items. [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] uses the templates when users create new projects and add new items to existing projects. For more information, see [Adding Project and Project Item Templates](../vs140/Adding-Project-and-Project-Item-Templates.md).  
  
-   Project types can support multiple configurations, such as Debug and Release. Users can change the different configurations of a project by using property pages that you supply. For more information, see [Managing Configuration Options](../vs140/Managing-Configuration-Options.md).  
  
## See Also  
 [Deploying Managed-Code Project Types](../vs140/Deploying-Project-Types.md)