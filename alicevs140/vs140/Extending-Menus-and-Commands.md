---
title: "Extending Menus and Commands"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7b2be4b9-e3fe-4412-874f-ae72ebc84c4b
caps.latest.revision: 51
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Extending Menus and Commands
Commands are the way you add actions and processes to Visual Studio. In most cases commands are displayed on menus or toolbars. The VSPackage project template shows how to implement a very basic command. For a slightly longer but still basic implementation, see [Creating a VSPackage with a Menu Command](../Topic/Creating%20an%20Extension%20with%20a%20Menu%20Command.md).  
  
 For more information about Visual Studio commands, menus and toolbars, see [Commands, Menus, and Toolbars](../Topic/Commands,%20Menus,%20and%20Toolbars.md).  
  
 Commands, menus, and toolbars are defined in the .vsct file that is part of VSPackage projects. You can find information about the Visual Studio IDE and the .vsct file in [How VSPackages Add User Interface Elements](../Topic/How%20VSPackages%20Add%20User%20Interface%20Elements.md).  
  
 The following topics explain how to add different kinds of commands, menus, and toolbars.  
  
## In This Section  
 [Adding a Menu to the Visual Studio Menu Bar](../vs140/Adding-a-Menu-to-the-Visual-Studio-Menu-Bar.md)  
 Explains how to add a menu to the top Visual Studio menu bar.  
  
 [Binding Keyboard Shortcuts to Menu Items](../vs140/Binding-Keyboard-Shortcuts-to-Menu-Items.md)  
 Explains how to add a keyboard shortcut (such as CTRL + 3) to a menu item.  
  
 [Adding a Submenu to a Menu](../vs140/Adding-a-Submenu-to-a-Menu.md)  
 Explains how to add a submenu to the top menu.  
  
 [Adding a Most Recently Used List to a Submenu](../vs140/Adding-a-Most-Recently-Used-List-to-a-Submenu.md)  
 Explains how to add a Most Recently Used list.  
  
 [How to: Create Reusable Groups of Buttons](../vs140/Creating-Reusable-Groups-of-Buttons.md)  
 Describes how to group command items so that they can be included on multiple menus.  
  
 [How to: Add Icons to Commands](../vs140/Adding-Icons-to-Menu-Commands.md)  
 Describes how to add an icon to a command on both a toolbar and a menu.  
  
 [How to: Change Text of Menus](../vs140/Changing-the-Text-of-a-Menu-Command.md)  
 Describes the use of the `TextChanges` flag to enable a menu item to be changed dynamically.  
  
 [How to: Change the Appearance of Commands](../vs140/Changing-the-Appearance-of-a-Command.md)  
 Describes how to dynamically enable or disable a command.  
  
 [How to: Update the User Interface](../Topic/Updating%20the%20User%20Interface.md)  
 Describes how to force an update of the user interface to reflect recent changes.  
  
 [Localizing Menu Commands](../vs140/Localizing-Menu-Commands.md)  
 Explains how to localize menu commands.  
  
## Related Sections