---
title: "IDE-Defined Commands, Menus, and Groups"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 86b3af13-7163-48c6-986b-7beeedbc26cc
caps.latest.revision: 29
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDE-Defined Commands, Menus, and Groups
Many menus, commands and command groups are already defined for use by the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] IDE. These commands are also available for your use when you extend [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
## Finding Environment-Defined Commands  
 The environment commands are defined in a set of four .vsct files:  
  
-   SharedCmdDef.vsct  
  
-   SharedCmdPlace.vsct  
  
-   ShellCmdDef.vsct  
  
-   ShellCmdPlace.vsct  
  
 These files are located in *<Visual Studio SDK installation path\>*\VisualStudioIntegration\Common\Inc\\. These files provide the definitions and GUIDs of the menus and groups that you can use in the command table configuration (.vsct) file of your VSPackage as containers for your own menus, groups, and commands.  
  
## In This Section  
 [GUIDs and IDs of Visual Studio Menus](../vs140/GUIDs-and-IDs-of-Visual-Studio-Menus.md)  
 Gives the GUID and ID values of menus on the Visual Studio menu bar, and of the groups they contain.  
  
 [GUIDs and IDs of Visual Studio Toolbars](../vs140/GUIDs-and-IDs-of-Visual-Studio-Toolbars.md)  
 Gives the GUID and ID values of toolbars in the Visual Studio IDE, and of the groups they contain.  
  
 [GUIDs and IDs of Visual Studio Commands](../vs140/GUIDs-and-IDs-of-Visual-Studio-Commands.md)  
 Gives the GUID and ID values of commands defined by the Visual Studio IDE.  
  
## See Also  
 [Visual Studio Command Table (.Vsct) Files](../vs140/Visual-Studio-Command-Table--.Vsct--Files.md)   
 [Environment-Defined Commands for Extending Project Systems](../Topic/IDE-Defined%20Commands%20for%20Extending%20Project%20Systems.md)   
 [How VSPackages Contribute User Interface Elements](../Topic/How%20VSPackages%20Add%20User%20Interface%20Elements.md)