---
title: "-Setup (devenv.exe)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
H1: /Setup (devenv.exe)
ms.assetid: 87608b7f-a156-400c-80f5-fc823f843e61
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Setup (devenv.exe)
Forces [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] to merge the resource metadata that describes menus, toolbars, and command groups, from all available VSPackages.  
  
## Syntax  
  
```  
devenv /setup  
```  
  
## Remarks  
 This switch takes no arguments. The `devenv /setup` command is typically given as the last step of the installation process. Use of the `/setup` switch does not start [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 You must run `devenv` as an administrator in order to use the [/setup (devenv.exe)](../vs140/-Setup--devenv.exe-.md) and [/InstallVSTemplates (devenv.exe)](../vs140/-InstallVSTemplates--devenv.exe-.md) switches.  
  
## Example  
 This example shows the last step in the installation of a version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] that includes VSPackages.  
  
```  
devenv /setup  
```  
  
## See Also  
 [Devenv Command Line Switches](../vs140/Devenv-Command-Line-Switches.md)