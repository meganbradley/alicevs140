---
title: "Services Provided (Source Control VSPackage)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9db07d70-87d2-4401-bc88-e3a49d81e9a2
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Services Provided (Source Control VSPackage)
Services are the primary mechanism through which functionality is shared among VSPackages and between the Visual Studio integrated development environment (IDE) and its installed VSPackages. For detailed description of services and their importance in the Visual Studio IDE, see[Visual Studio Services](../Topic/Using%20and%20Providing%20Services.md).  
  
## The Source Control Service  
 Visual Studio provides two layers of services, IDE-level services and package-level services. The Visual Studio IDE natively provides IDE-level services. The source control package consumes some of these services. The source control package as a VSPackage shares its source control functionality by providing a private source control service of its own. The source control package encapsulates the set of source control-related interfaces implemented by it in the form of a contract that can be used by the Visual Studio IDE.  
  
## See Also  
 [VSIP Design Elements](../vs140/Source-Control-VSPackage-Design-Elements.md)