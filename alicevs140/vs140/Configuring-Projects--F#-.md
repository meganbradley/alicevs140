---
title: "Configuring Projects (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: a1489abb-6294-4f8f-b71f-2cb126393526
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Configuring Projects (F#)
This topic includes information about how to use the **Project Designer** when you work with F# projects. Working with F# projects is not significantly different from working with Visual Basic or C# projects. You can often use the general Visual Studio project documentation as your primary reference when you use F#. This topic provides links to relevant information in the Visual Studio documentation for settings that are shared with the other [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] languages, and also describes the settings specific to F#.  
  
## Project Designer  
 The **Project Designer** and its general use are described fully in the topic [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7) in the Visual Studio documentation. The **Project Designer** consists of several pages grouped by related functionality. The pages available for F# projects are mostly a subset of those available for other languages. The pages supported in F# are described in the following table. The pages that are not available relate to features that are not available in F#, or that are available only by changing a command-line option. The pages that are available in F# resemble the C# pages most closely, so a link is provided to the relevant C# **Project Designer** page.  
  
|Project Designer page|Related links|Description|  
|---------------------------|-------------------|-----------------|  
|**Application**|[Application Page, Project Designer (C#)](../Topic/Application%20Page,%20Project%20Designer%20\(C%23\).md)|Enables you to specify application-level settings and properties, such as whether you are creating a library or an executable file, what version of the .NET Framework the application is targeting, and information about where the resource files that the application uses are stored.|  
|**Build**|[Build Page, Project Designer (C#)](../Topic/Build%20Page,%20Project%20Designer%20\(C%23\).md)|Enables you to control how the code is compiled.|  
|**Build Events**|[Build Events Page, Project Designer (C#)](../vs140/Build-Events-Page--Project-Designer--C#-.md)|Enables you to specify commands to run before or after a compilation.|  
|**Debug**|[Debug Page, Project Designer](../vs140/Debug-Page--Project-Designer.md)|Enables you to control how the application runs during debugging. This includes what command-line to use and what your application's starting directory is, and any special debugging modes you want to enable, such as native code and SQL.|  
|**Reference Paths**|[Managing Project References](../Topic/Managing%20references%20in%20a%20project.md)|Enables you to specify where to search for assemblies that the code depends on.|  
  
## F#-Specific Settings  
 The following table summarizes settings that are specific to F#.  
  
|Project Designer page|Setting|Description|  
|---------------------------|-------------|-----------------|  
|**Build**|**Generate tail calls**|If selected, enables the use of the tail Microsoft intermediate language (MSIL) instruction. This causes the stack frame to be reused for tail recursive functions. Equivalent to the `--tailcalls` compiler option.|  
|**Build**|**Other flags**|Allows you to specify additional compiler command-line options.|  
  
## See Also  
 [Writing F# Programs with Visual Studio](../vs140/Using-Visual-Studio-to-Write-F#-Programs.md)   
 [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md)   
 [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7)