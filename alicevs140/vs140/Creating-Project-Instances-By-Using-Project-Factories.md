---
title: "Creating Project Instances By Using Project Factories"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 94c90012-8669-459c-af8e-307ac242c8c4
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Creating Project Instances By Using Project Factories
Project types in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] use a *project factory* to create instances of project objects. A project factory is similar to a standard class factory for cocreatable COM objects. However, project objects are not cocreatable: they can only be created by using a project factory.  
  
 The [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] IDE calls the project factory implemented in your VSPackage when a user loads an existing project or creates a new project in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. The new project object provides the IDE with enough information to populate Solution Explorer. The new project object also provides the required interfaces for supporting all relevant UI actions initiated by the IDE.  
  
 You can implement the <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory?qualifyHint=False> interface in a class in your project. Typically, it resides in its own module.  
  
 For an example of an implementation of the `IVsProjectFactory` interface, see PrjFac.cpp that is contained in the [Basic Project](assetId:///385fd2a3-d9f1-4808-87c2-a3f05a91fc36) sample directory.  
  
 Projects that support being aggregated by an owner must persist an owner key in their project file. When the <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory.CreateProject?qualifyHint=False> method is called on a project with an owner key, the owned project converts its owner key to a project factory GUID then calls the `CreateProject` method on this project factory to do the actual creation.  
  
## Creating an Owned Project  
 An owner creates an owned project in two phases:  
  
1.  By calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsOwnedProjectFactory.PreCreateForOwner?qualifyHint=False> method. This gives the owned project a chance to create an aggregated project object based on the input controlling `IUnknown`. The owned project passes the inner `IUnknown` and the aggregated object back to the owner project. This gives the owned project a chance to store the inner `IUnknown`.  
  
2.  By calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsOwnedProjectFactory.InitializeForOwner?qualifyHint=False> method. The owned project does all its instantiation when this method is called instead of calling `IVsProjectFactory::CreateProject` as would be the case for projects that are not owned. The input `VSOWNEDPROJECTOBJECT` enumeration is typically the aggregated owned project. The owned project can use this variable to determine whether its project object has already been created (cookie does not equal NULL) or must be created (cookie equals NULL).  
  
 Project types are identified by a unique project GUID, similar to the CLSID of a cocreatable COM object. Typically, one project factory handles creating instances of a single project type, although it is possible to have one project factory handle more than one project type GUID.  
  
 Project types are associated with a particular file name extension. When a user attempts to open an existing project file or attempts to create a new project by cloning a template, the IDE uses the extension on the file to determine the corresponding project GUID.  
  
 As soon as the IDE determines whether it must create a new project or open an existing project of a particular type, the IDE uses the information in the system registry under [HKEY_LOCAL_MACHINE\Software\Microsoft\VisualStudio\8.0\Projects] to find which VSPackage implements the required project factory. The IDE loads this VSPackage. In the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite?qualifyHint=False> method, the VSPackage must register its project factory with the IDE by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsRegisterProjectTypes.RegisterProjectType?qualifyHint=False> method.  
  
 The primary method of the `IVsProjectFactory` interface is <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory.CreateProject?qualifyHint=False> which should handle two scenarios: opening an existing project and creating a new project. Most projects store their project state in a project file. Typically, new projects are created by making a copy of the template file passed to the `CreateProject` method and then opening the copy. Existing projects are instantiated by directly opening the project file passed to `CreateProject` method. The `CreateProject` method can display additional UI features to the user as necessary.  
  
 A project can also use no files and, instead, store its project state in a storage mechanism other than the file system, such as a database or Web server. In this case, the file name parameter passed to the `CreateProject` method is not actually a file system path but a unique string—a URL—to identify the project data. You do not need to copy the template files that are passed to `CreateProject` to trigger the appropriate construction sequence to be executed.  
  
## See Also  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsOwnedProjectFactory?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsRegisterProjectTypes?qualifyHint=False>   
 [Checklist: Creating New Project Types](../Topic/Checklist:%20Creating%20New%20Project%20Types.md)