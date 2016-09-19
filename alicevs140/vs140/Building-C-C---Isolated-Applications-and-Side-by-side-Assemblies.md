---
title: "Building C-C++ Isolated Applications and Side-by-side Assemblies"
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
H1: Building C/C++ Isolated Applications and Side-by-side Assemblies
ms.assetid: 9465904e-76f7-48bd-bb3f-c55d8f1699b6
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Building C-C++ Isolated Applications and Side-by-side Assemblies
Visual C++ supports a deployment model for Windows client applications based on the idea of [isolated applications](http://msdn.microsoft.com/library/aa375190) and [side-by-side assemblies](-win32-side-by-side-assemblies). By default, Visual C++ builds all native C/C++ applications as isolated applications that use [manifests](http://msdn.microsoft.com/library/aa375365) to describe their dependencies on Visual C++ libraries.  
  
 Building C/C++ programs as isolated applications presents a range of advantages. For example, an isolated application is unaffected when other C/C++ applications install or uninstall Visual C++ libraries. Visual C++ libraries used by isolated applications may still be redistributed in either the application's local folder, or by installation to the native assembly cache (WinSxS); however, servicing of Visual C++ libraries for already deployed applications can be simplified by using a [publisher configuration file](http://msdn.microsoft.com/library/aa375680). The isolated application deployment model makes it easier to ensure that C/C++ applications that are running on a specific computer use the most recent version of Visual C++ libraries, while still leaving open the possibility for system administrators and application authors to control explicit version binding of applications to their dependent DLLs.  
  
 This section discusses how you can build your C/C++ application as an isolated application and ensure that it binds to Visual C++ libraries using a manifest. The information in this section primarily applies to native, or unmanaged, Visual C++ applications. For information about deploying native applications built with Visual C++, see [Redistributing Visual C++ Files](../vs140/Redistributing-Visual-C---Files.md).  
  
## In This Section  
 [Concepts of Isolated Assemblies and Side-by-side Assemblies](../vs140/Concepts-of-Isolated-Applications-and-Side-by-side-Assemblies.md)  
  
 [Building C/C++ Isolated Applications](../vs140/Building-C-C---Isolated-Applications.md)  
  
 [Building C/C++ Side-by-side Assemblies](../vs140/Building-C-C---Side-by-side-Assemblies.md)  
  
 [How to: Build Registration-Free COM Components](../vs140/How-to--Build-Registration-Free-COM-Components.md)  
  
 [How to: Build Isolated Applications to Consume COM Components](../vs140/How-to--Build-Isolated-Applications-to-Consume-COM-Components.md)  
  
 [Understanding Manifest Generation for C/C++ Programs](../vs140/Understanding-Manifest-Generation-for-C-C---Programs.md)  
  
 [Troubleshooting](../vs140/Troubleshooting-C-C---Isolated-Applications-and-Side-by-side-Assemblies.md)  
  
## Related Sections  
 [Isolated Applications and Side-by-side Assemblies](http://msdn.microsoft.com/library/dd408052)  
  
 [Deployment (C++)](../vs140/Deploying-Native-Desktop-Applications--Visual-C---.md)