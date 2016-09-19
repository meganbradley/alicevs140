---
title: "Default Command, Group, and Toolbar Placement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 35342110-d639-4577-8367-00b21dcc6f07
caps.latest.revision: 32
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Default Command, Group, and Toolbar Placement
For product uniformity and stability, the UI displays certain command groups by default, and [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] provides definitions for commands and command groups. VSPackages can also use the standard commands and command groups.  
  
 The default command groups fall into three categories: IDE commands, product commands, and editor commands.  
  
## Default IDE Commands  
 The default IDE toolbar includes commands shared by all products contained in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. These include commands relating to generic project operations, such as the **Save** command and the **Add Item** command. VSPackages should not add to or subtract from this toolbar, with one exception: If the product or VSPackage adds a new tool window, then the window should be added to the list of available tool windows on the **View** menu. New products or VSPackages can add their own toolbar.  
  
## Default Product Commands  
 Each product can provide the IDE with its own default toolbar that contains important and frequently used commands. It is best, however, to use existing menus and toolbars whenever possible and supplement them with other task-specific toolbars as needed.  
  
 The priority field for a toolbar determines its row placement. Zero priority places the toolbar on the third row (row 3), beneath the menu bar (row 1) and the **Standard** toolbar (row 2). Therefore, other toolbars appear at row (priority + 3). Subsequent toolbars are placed on the same row, if there is room; otherwise, they are automatically moved to the next row.  
  
## Default Editor Commands  
 A VSPackage that provides a custom editor should provide a default toolbar that contains the most important and frequently used commands in that editor. The editor toolbar should appear when the editor is active and should be hidden when the editor is not active. This visibility is controlled in the `VisibilityConstraints Element` of the .vsct file.  
  
 Editor toolbars should be placed below IDE and product toolbars.  
  
## See Also  
 [IDE-Defined Commands](../vs140/IDE-Defined-Commands--Menus--and-Groups.md)   
 [How VSPackages Contribute User Interface Elements](../Topic/How%20VSPackages%20Add%20User%20Interface%20Elements.md)