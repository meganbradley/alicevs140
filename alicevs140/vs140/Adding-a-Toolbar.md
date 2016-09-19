---
title: "Adding a Toolbar"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 17302c25-6f59-4e97-8c85-54f95336a07f
caps.latest.revision: 40
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Adding a Toolbar
This walkthrough shows how to add a toolbar to the Visual Studio IDE.  
  
 A toolbar is a horizontal or vertical strip that contains buttons that are bound to commands. Depending on its implementation, a toolbar in the IDE can be repositioned, docked on any side of the main IDE window, or made to stay in front of other windows.  
  
 In addition, users can add commands to a toolbar or remove them from it by using the **Customize** dialog box. Typically, toolbars in VSPackages are user-customizable. The IDE handles all customization, and the VSPackage responds to commands. The VSPackage does not have to know where a command is physically located.  
  
 For more information about menus, see [Menu and Toolbar Commands](../Topic/Commands,%20Menus,%20and%20Toolbars.md).  
  
## Prerequisites  
 Starting in Visual Studio 2015, you do not install the Visual Studio SDK from the download center. It is included as an optional feature in Visual Studio setup. You can also install the VS SDK later on. For more information, see [Installing the Visual Studio SDK](../vs140/Installing-the-Visual-Studio-SDK.md).  
  
## Creating an Extension with a Toolbar  
 Create a VSIX project named `IDEToolbar`. Add a menu command item template named **ToolbarTestCommand**. For information about how to do this, see [Creating an Extension with a Menu Command](../Topic/Creating%20an%20Extension%20with%20a%20Menu%20Command.md).  
  
## Creating a Toolbar for the IDE  
  
1.  In ToolbarTestCommandPackage.vsct, look for the Symbols section. In the GuidSymbol element named guidToolbarTestCommandPackageCmdSet, add declarations for a toolbar and a toolbar group, as follows.  
  
    ```xml  
    <IDSymbol name="Toolbar" value="0x1000" />  
    <IDSymbol name="ToolbarGroup" value="0x1050" />  
  
    ```  
  
2.  At the top of the Commands section, create a Menus section. Add a Menu element to the Menus section to define your toolbar.  
  
    ```xml  
    <Menus>  
        <Menu guid="guidToolbarTestCommandPackageCmdSet" id="Toolbar"  
            type="Toolbar" >  
            <CommandFlag>DefaultDocked</CommandFlag>  
            <Strings>  
                <ButtonText>Test Toolbar</ButtonText>  
                <CommandName>Test Toolbar</CommandName>  
            </Strings>  
          </Menu>  
    </Menus>  
    ```  
  
     Toolbars cannot be nested like submenus. Therefore, you do not have to assign a parent group. Also, you do not have to set a priority, because the user can move toolbars. Typically, initial placement of a toolbar is defined programmatically, but subsequent changes by the user are persisted.  
  
3.  In the [Groups](../vs140/Groups-Element.md) section, after the existing group entry, define a [Group](../vs140/Group-Element.md) element to contain the commands for the toolbar.  
  
    ```xml  
    <Group guid="guidToolbarTestCommandPackageCmdSet" id="ToolbarGroup"  
          priority="0x0000">  
      <Parent guid="guidToolbarTestCommandPackageCmdSet" id="Toolbar"/>  
    </Group>  
    ```  
  
4.  Make the button appear on the toolbar. In the Buttons section, replace the Parent block in the Button to the toolbar. The resulting Button block should look like this:  
  
    ```xml  
    <Button guid="guidToolbarTestCommandPackageCmdSet" id="ToolbarTestCommandId" priority="0x0100" type="Button">  
        <Parent guid= "guidToolbarTestCommandPackageCmdSet" id="ToolbarGroup" />  
                <Icon guid="guidImages" id="bmpPic1" />  
        <Strings>  
            <ButtonText>Invoke ToolbarTestCommand</ButtonText>  
        </Strings>  
    </Button>  
    ```  
  
     By default, if a toolbar has no commands, it does not appear.  
  
5.  Build the project and start debugging. The experimental instance should appear.  
  
6.  Right-click the Visual Studio menu bar to get the list of toolbars. Select **Test Toolbar**.  
  
7.  You should now see your toolbar as an icon to the right of the Find in Files icon. When you click the icon, you should see a message box that says **ToolbarTestCommandPackage. Inside IDEToolbar.ToolbarTestCommand.MenuItemCallback()**.  
  
## See Also  
 [Menu and Toolbar Commands](../Topic/Commands,%20Menus,%20and%20Toolbars.md)