---
title: "Registering File Name Extensions for Side-By-Side Deployments"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9ab046a2-147d-4167-aa14-7d661b1eaaa5
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Registering File Name Extensions for Side-By-Side Deployments
For VSPackages deployed in a side-by-side environment, you must register file name extensions to associate the files with the correct version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. Unless you use a version-specific file name extension, registration enables users to open your project and project item files in the appropriate version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
## In This Section  
 [About File Name Extensions](../vs140/About-File-Name-Extensions.md)  
 Discusses how file name extensions are registered.  
  
 [Specifying File Handlers for File Name Extensions](../vs140/Specifying-File-Handlers-for-File-Name-Extensions.md)  
 Provides information about how to register the applications that can open, edit, and so on, a particular file name extension.  
  
 [Registering Verbs for File Extensions](../vs140/Registering-Verbs-for-File-Name-Extensions.md)  
 Discusses how to register verbs.  
  
 [Managing Side-by-Side File Associations](../vs140/Managing-Side-by-Side-File-Associations.md)  
 Discusses how to handle side-by-side installations in which a particular version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] should be invoked to open a file.  
  
## Related Sections  
 [Supporting Multiple Versions of Visual Studio](../vs140/Supporting-Multiple-Versions-of-Visual-Studio.md)  
 Describes issues related to multiple versions of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] and your VSPackage during development and deployment to end users.