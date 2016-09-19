---
title: "-Edit (devenv.exe)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
H1: /Edit (devenv.exe)
ms.assetid: 02b3d6e7-a2b1-4d83-a747-aa8c2fb758b7
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Edit (devenv.exe)
Opens the specified file in an existing instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
## Syntax  
  
```  
Devenv /edit [file1[ file2]]  
```  
  
## Arguments  
 `file1`  
 Optional. The file to open in an existing instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. If no instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] exists, a new instance is created with a simplified window layout, and `file1` is opened in the new instance.  
  
 `file2`  
 Optional. One or more additional files to open in the existing instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
## Remarks  
 If no file is specified and there is an existing instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], the existing instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] receives focus. If no file is specified and there is no existing instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], a new instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] is created with a simplified window layout.  
  
 If the existing instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] is in a modal state, for example, if the [Options dialog box](../vs140/Options-Dialog-Box--Visual-Studio-.md) is open, the file will open in the existing instance when [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] exits the modal state.  
  
## Example  
 This example opens the file `MyFile.cs` in an existing instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] or opens the file in a new instance of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] if one does not already exist.  
  
```  
devenv /edit MyFile.cs  
```  
  
## See Also  
 [Devenv Command Line Switches](../vs140/Devenv-Command-Line-Switches.md)