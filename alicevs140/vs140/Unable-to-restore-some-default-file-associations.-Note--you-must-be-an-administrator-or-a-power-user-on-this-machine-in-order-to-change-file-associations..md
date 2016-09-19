---
title: "Unable to restore some default file associations. Note: you must be an administrator or a power user on this machine in order to change file associations."
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 449c5608-83e3-4ddd-91f1-1061916995b3
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Unable to restore some default file associations. Note: you must be an administrator or a power user on this machine in order to change file associations.
This error occurs when the devenv command-line switch /AssociateFiles is used, but the current user rights do not allow access to the HKEY_CLASSES_ROOT section of the registry. When you run [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] on [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)], you must run devenv as an administrator to use the /AssociateFiles (devenv.exe) switch.  
  
### To correct this error  
  
-   Change to administrative credentials and try again.  
  
## See Also  
 [User Rights and Visual Studio](assetId:///d5c55084-1e7b-4b61-b478-137db01c0fc0)   
 [Devenv Command Line Switches](../vs140/Devenv-Command-Line-Switches.md)