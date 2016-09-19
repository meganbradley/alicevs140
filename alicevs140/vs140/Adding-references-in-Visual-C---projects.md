---
title: "Adding references in Visual C++ projects"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 12b8f571-0f21-40b3-9404-5318a57e9cb5
caps.latest.revision: 34
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Adding references in Visual C++ projects
It is very common for programs to call into APIs in other binaries such as DLLs, Windows Runtime components, extension SDKs, COM components, and .NET assemblies. The way that your program finds those other binaries depends both on the type of your project, and the type of the binary.  
  
 In a native C++ project, if you are consuming a native DLL or COM component that is not being produced by another project in your solution, you use LoadLibrary or CoCreateInstance to specify the path to the binary, or else let the system locate it by looking in specific well-defined locations.  
  
 In other types of projects such as UWP projects or C++/CLI projects, or when the binary is produced by another project in your solution, you add a *reference* to the assembly,  component or project.   A reference is essentially a set of data that enables your program to locate and communicate with the binary.       When you add a reference, Visual Studio handles the low level details. To set references from a C++ project to [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] assemblies (C++/CLI only), COM components, other projects in your solution including shared projects, or connected services,  right-click on the **References** node in **Solution Explorer** to bring up the **Reference Manager**. What you see in Reference Manager differs depending on your project type.  
  
 In a native C++ project (ATL) the concept of *references* only applies to other projects in the solution, including shared projects, so that is all you see in **Reference Manager**:  
  
 ![Visual C&#43;&#43; Reference Manager &#40;ATL Projects&#41;](../vs140/media/Visual-C---Reference-Manager--ATL-Projects-.png "Visual C++ Reference Manager (ATL Projects)")  
  
 In a C++/CLI or Universal Windows Platform project,  the concept of references applies to more kinds of binaries in addition to other projects in the solution.  These are all exposed in **Reference Manager**:  
  
 ![Visual C&#43;&#43; Reference Manager for C&#43;&#43;&#47;CLI projects](../Image/Visual%20C++%20Reference%20Manager%20for%20C++/CLI%20projects.png "Visual C++ Reference Manager for C++/CLI projects")  
  
## Reference properties  
 Each kind of reference has properties. You can view the properties by selecting the reference in Solution Explorer and pressing **Alt + Enter**, or else right-clicking and choosing **Properties**. Some properties are read-only and some can be modified. However, typically you don't have to manually modify these properties.  
  
### ActiveX reference properties  
 ActiveX reference properties are available only for references to COM components. These properties are displayed only when a COM component is selected in the **References** pane. The properties cannot be modified.  
  
 **Control Full Path**  
 Displays the directory path of the referenced control.  
  
 **Control GUID**  
 Displays the GUID for the ActiveX control.  
  
 **Control Version**  
 Displays the version of the referenced ActiveX control.  
  
 **Type Library Name**  
 Displays the name of the referenced type library.  
  
 **Wrapper Tool**  
 Displays the tool that is used to build the interop assembly from the referenced COM library or ActiveX control.  
  
### Assembly reference properties  
 Assembly reference properties are available only for references to [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] assemblies in C++/CLI projects. These properties are displayed only when a [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] assembly is selected in the **References** pane. The properties cannot be modified.  
  
 **Relative Path**  
 Displays the relative path from the project directory to the referenced assembly.  
  
### Build properties  
 The following properties are available on various kinds of references. They enable you to specify how to build with references.  
  
 **Copy Local**  
 Specifies whether to automatically copy the referenced assembly to the target location during a build.  
  
 **Copy Local Satellite Assemblies**  
 Specifies whether to automatically copy the satellite assemblies of the referenced assembly to the target location during a build. Only used if **Copy Local** is `true`.  
  
 **Reference Assembly Output**  
 Specifies that this assembly is used in the build process. If `true`, the assembly is used on the compiler command line during the build.  
  
### Project-to-project reference properties  
 The following properties define a *project-to-project reference* from the project that is selected in the **References** pane to another project  in the same solution. For more information, see [Managing Project References](../Topic/Managing%20references%20in%20a%20project.md).  
  
 **Link Library Dependencies**  
 When this property is **True**, the project system links into the dependent project the .lib files that are produced by the independent project. Typically, you will specify **True**.  
  
 **Project Identifier**  
 Uniquely identifies the independent project. The property value is an internal system GUID that cannot be modified.  
  
 **Use Library Dependency Inputs**  
 When this property is **False**, the project system will not link into the dependent project the .obj files for the library produced by the independent project. Consequently, this value disables incremental linking. Typically, you will specify **False** because building the application can take a long time if there are many independent projects.  
  
### Reference properties  
 The following properties are found on COM and .NET assembly references, and cannot be modified.  
  
 **Assembly Name**  
 Displays the assembly name for the referenced assembly.  
  
 **Culture**  
 Displays the culture of the selected reference.  
  
 **Description**  
 Displays the description of the selected reference.  
  
 **Full Path**  
 Displays the directory path of the referenced assembly.  
  
 **Identity**  
 For the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] assemblies, displays the full path. For COM components, displays the GUID.  
  
 **Label**  
 Displays the label of the reference.  
  
 **Name**  
 Displays the name of the reference.  
  
 **Public Key Token**  
 Displays the public key token that is used to identify the referenced assembly.  
  
 **Strong Name**  
 `true` if the referenced assembly has a strong name. A strong named assembly is uniquely versioned.  
  
 **Version**  
 Displays the version of the referenced assembly.  
  
## See Also  
 [Property Pages (C++)](../vs140/Property-Pages--Visual-C---.md)   
 [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md)