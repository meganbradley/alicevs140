---
title: "Assemblies and the Global Assembly Cache (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fcf78ff1-f1ab-4a5d-b6d8-00d2046b6c80
caps.latest.revision: 5
---
# Assemblies and the Global Assembly Cache (Visual Basic)
Assemblies form the fundamental unit of deployment, version control, reuse, activation scoping, and security permissions for a .NET-based application. Assemblies take the form of an executable (.exe) file or dynamic link library (.dll) file, and are the building blocks of the .NET Framework. They provide the common language runtime with the information it needs to be aware of type implementations. You can think of an assembly as a collection of types and resources that form a logical unit of functionality and are built to work together.  
  
 Assemblies can contain one or more modules. For example, larger projects may be planned in such a way that several individual developers work on separate modules, all coming together to create a single assembly. For more information about modules, see the topic [How to: Build a Multifile Assembly](assetId:///261c5583-8a76-412d-bda7-9b8ee3b131e5).  
  
 Assemblies have the following properties:  
  
-   Assemblies are implemented as .exe or .dll files.  
  
-   You can share an assembly between applications by putting it in the global assembly cache. Assemblies must be strong-named before they can be included in the global assembly cache. For more information, see [Strong-Named Assemblies](assetId:///d4a80263-f3e0-4d81-9b61-f0cbeae3797b).  
  
-   Assemblies are only loaded into memory if they are required. If they are not used, they are not loaded. This means that assemblies can be an efficient way to manage resources in larger projects.  
  
-   You can programmatically obtain information about an assembly by using reflection. For more information, see [Reflection (Visual Basic)](../Topic/Reflection%20\(Visual%20Basic\).md).  
  
-   If you want to load an assembly only to inspect it, use a method such as <xref:System.Reflection.Assembly.ReflectionOnlyLoadFrom?qualifyHint=False>.  
  
## Assembly Manifest  
 Within every assembly is an *assembly manifest*. Similar to a table of contents, the assembly manifest contains the following:  
  
-   The assembly's identity (its name and version).  
  
-   A file table describing all the other files that make up the assembly, for example, any other assemblies you created that your .exe or .dll file relies on, or even bitmap or Readme files.  
  
-   An *assembly reference list*, which is a list of all external dependencies—.dlls or other files your application needs that may have been created by someone else. Assembly references contain references to both global and private objects. Global objects reside in the global assembly cache, an area available to other applications, somewhat like the System32 directory. The <xref:Microsoft.VisualBasic?qualifyHint=True> namespace is an example of an assembly in the global assembly cache. Private objects must be in a directory at either the same level as or below the directory in which your application is installed.  
  
 Because assemblies contain information about content, versioning, and dependencies, the applications you create with Visual Basic do not rely on Windows registry values to function properly. Assemblies reduce .dll conflicts and make your applications more reliable and easier to deploy. In many cases, you can install a .NET-based application simply by copying its files to the target computer.  
  
 For more information see [Assembly Manifest](assetId:///8e40fab9-549d-4731-aec2-ffa47a382de0).  
  
## Adding a Reference to an Assembly  
 To use an assembly, you must add a reference to it. Next, you use the [Imports statement](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md) to choose the namespace of the items you want to use. Once an assembly is referenced and imported, all the accessible classes, properties, methods, and other members of its namespaces are available to your application as if their code were part of your source file.  
  
## Creating an Assembly  
 Compile your application by building it from the command line using the command-line compiler. For details about building assemblies from the command line, see [Building from the Command Line](../vs140/Building-from-the-Command-Line--Visual-Basic-.md).  
  
> [!NOTE]
>  To build an assembly in Visual Studio, on the **Build** menu choose **Build**.  
  
## See Also  
 [Visual Basic Programming Guide](../vs140/Visual-Basic-Programming-Guide.md)   
 [Assemblies in the Common Language Runtime](assetId:///2cfebe19-7436-49f1-bd99-3c4019f0b676)   
 [Friend Assemblies (Visual Basic)](../Topic/Friend%20Assemblies%20\(Visual%20Basic\).md)   
 [How to: Share an Assembly with Other Applications (Visual Basic)](../vs140/How-to--Share-an-Assembly-with-Other-Applications--Visual-Basic-.md)   
 [How to: Load and Unload Assemblies (Visual Basic)](../vs140/How-to--Load-and-Unload-Assemblies--Visual-Basic-.md)   
 [How to: Determine If a File Is an Assembly (Visual Basic)](../vs140/How-to--Determine-If-a-File-Is-an-Assembly--Visual-Basic-.md)   
 [How to: Create and Use Assemblies Using the Command Line (Visual Basic)](../vs140/How-to--Create-and-Use-Assemblies-Using-the-Command-Line--Visual-Basic-.md)   
 [Walkthrough: Embedding Types from Managed Assemblies (Visual Basic)](../Topic/Walkthrough:%20Embedding%20Types%20from%20Managed%20Assemblies%20in%20Visual%20Studio%20\(Visual%20Basic\).md)   
 [Walkthrough: Embedding Type Information from Microsoft Office Assemblies (Visual Basic)](../vs140/Walkthrough--Embedding-Type-Information-from-Microsoft-Office-Assemblies-in-Visual-Studio--Visual-Basic-.md)