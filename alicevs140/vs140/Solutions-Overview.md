---
title: "Solutions Overview"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b21e3a1-170a-4485-941e-6b04b7b27886
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Solutions Overview
A solution is a grouping of one or more projects that work together to create an application. The project and status information pertaining to the solution are stored in two different solution files. The solution (.sln) file is text-based and can be placed under source code control and shared between users. The solution user option (.suo) file is binary. As a result, the .suo file cannot be placed under source code control and contains user-specific information.  
  
 Any VSPackage can write to either type of solution file. Because of the nature of the files, there are two different interfaces implemented to write to them. The <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionProps?qualifyHint=False> interface writes text information to the .sln file and the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts?qualifyHint=False> interface writes binary streams to the .suo file.  
  
> [!NOTE]
>  A project does not have to explicitly write an entry for itself into the solution file; the environment handles that for the project. Therefore, unless you want to add additional content specifically to the solution file, you do not need to register your VSPackage in this way.  
  
 Each VSPackage supporting solution persistence uses three interfaces, the <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionPersistence?qualifyHint=False> interface, which is implemented by the environment and called by the VSPackage, and `IVsPersistSolutionProps` and `IVsPersistSolutionOpts`, which are both implemented by the VSPackage. The `IVsPersistSolutionOpts` interface only needs to be implemented if private information is to be written by the VSPackage to the .suo file.  
  
 When a solution is opened, the following process takes place.  
  
1.  The environment reads the solution.  
  
2.  If the environment finds a `CLSID`, it loads the corresponding VSPackage.  
  
3.  If a VSPackage is loaded, the environment calls `QueryInterface` for <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage?qualifyHint=False> interface, for the interface that the VSPackage requires.  
  
    1.  When reading from an .sln file, the environment calls `QueryInterface` for `IVsPersistSolutionProps`.  
  
    2.  When reading from an .suo file, the environment calls `QueryInterface` for `IVsPersistSolutionOpts`.  
  
 Specific information relating to the use of these files can be found in [Solution (.Sln) File](../vs140/Solution--.Sln--File.md) and [Solution User Options (.Suo) File](../Topic/Solution%20User%20Options%20\(.Suo\)%20File.md).  
  
> [!NOTE]
>  If you want to create a new solution configuration consisting of two projects' configurations and excluding a third from the build, you need to use the Property Pages UI or automation. You can’t change the solution build manager configurations and their properties directly, but you can manipulate the solution build manager using the `SolutionBuild` class from DTE in the automation model. For more information about configuring solutions, see [Solution Configuration](../vs140/Solution-Configuration.md).  
  
## See Also  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionProps?qualifyHint=False>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionPersistence?qualifyHint=False>