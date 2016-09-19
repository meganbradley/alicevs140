---
title: "Deploying Native Desktop Applications (Visual C++)"
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
ms.assetid: 37f1691e-d67c-41e4-926e-528a237a9bac
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Deploying Native Desktop Applications (Visual C++)
Deployment is the process by which you distribute a finished application or component to be installed on other computers. Deployment planning starts when an application is created on a developer's computer. Deployment ends when the application is installed and ready to run on a user's computer.  
  
 Visual Studio provides different technologies for deploying Windows applications. These include [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] deployment and Windows Installer deployment.  
  
-   [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] can be used to deploy C++ applications that target the common language runtime (CLR)—mixed, pure, and verifiable assemblies. Although you can use Windows Installer to deploy a managed application, we recommend that you use [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] because it takes advantage of .NET Framework security features such as manifest signing. [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] does not support deployment of native C++ applications. For more information, see [ClickOnce Deployment for Visual C++ Applications](../vs140/ClickOnce-Deployment-for-Visual-C---Applications.md).  
  
-   Windows Installer technology can be used to deploy either native C++ applications or C++ applications that target the CLR.  
  
 The articles in this section of the documentation discuss how to ensure that a native Visual C++ application runs on any computer that provides a supported target platform, which files you must include in an installation package, and the recommended ways to redistribute the components that your application depends on.  
  
## In This Section  
 [Deployment in Visual C++](../vs140/Deployment-in-Visual-C--.md)  
  
 [Deployment Concepts](../vs140/Deployment-Concepts.md)  
  
 [Understanding Dependencies of a Visual C++ Application](../vs140/Understanding-the-Dependencies-of-a-Visual-C---Application.md)  
  
 [Determining Which DLLs to Redistribute](../vs140/Determining-Which-DLLs-to-Redistribute.md)  
  
 [Choosing a Deployment Method](../vs140/Choosing-a-Deployment-Method.md)  
  
 [Redistributing Visual C++ Files](../vs140/Redistributing-Visual-C---Files.md)  
  
 [Deployment Examples](../vs140/Deployment-Examples.md)  
  
 [Redistributing Web Applications](../vs140/Redistributing-Web-Client-Applications.md)  
  
 [ClickOnce Deployment for Visual C++ Applications](../vs140/ClickOnce-Deployment-for-Visual-C---Applications.md)  
  
 [Running a C++ /clr Application on a Previous Runtime Version](../vs140/Running-a-C----clr-Application-on-a-Previous-Runtime-Version.md)  
  
## Related Sections  
 [Building C/C++ Isolated Applications and Side-by-side Assemblies](../vs140/Building-C-C---Isolated-Applications-and-Side-by-side-Assemblies.md)  
  
 [Deploying .NET Framework Applications](assetId:///238d8284-6042-4a38-a7f6-1ee8efd719da)  
  
 [Troubleshooting C/C++ Isolated Applications and Side-by-side Assemblies](../vs140/Troubleshooting-C-C---Isolated-Applications-and-Side-by-side-Assemblies.md)