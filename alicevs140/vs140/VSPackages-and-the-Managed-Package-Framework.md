---
title: "VSPackages and the Managed Package Framework"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e8d80e0f-6b5b-4baf-a7df-59fd808c60cd
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# VSPackages and the Managed Package Framework
You can reduce development time by creating a VSPackage with the managed package framework (MPF) classes instead of by using COM interop classes.  
  
 There are two ways to create a managed VSPackage:  
  
-   Use the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Package project template  
  
     For more information, see [Walkthrough: Create a Menu Command with the Visual Studio Package Template](../vs140/Walkthrough--Creating-a-Menu-Command-By-Using-the-Visual-Studio-Package-Template.md).  
  
-   Build your VSPackage without the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Package project template  
  
     For example, you can copy a sample VSPackage and change the GUIDs and the names. You can find samples in the VSX section of [Code Gallery](http://code.msdn.microsoft.com/vsx/).  
  
## In This Section  
 [VSIP Managed Package Framework Classes](../Topic/Managed%20Package%20Framework%20Classes.md)  
 Describes and lists the MPF class namespaces and DLL files.  
  
## Related Sections  
 [How to: Create VSPackages (C#)](../vs140/Walkthrough--Creating-a-Menu-Command-By-Using-the-Visual-Studio-Package-Template.md)  
 Explains how to create a managed VSPackage.  
  
 [Managed VSPackages](../vs140/Managed-VSPackages.md)  
 Introduces aspects of VSPackages that apply to managed code.