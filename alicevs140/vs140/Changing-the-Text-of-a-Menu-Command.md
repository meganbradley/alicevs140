---
title: "Changing the Text of a Menu Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5cb676a0-c6e2-47e5-bd2b-133dc8842e46
caps.latest.revision: 27
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Changing the Text of a Menu Command
The following steps show how to change the text label of a menu command by using the <xref:System.ComponentModel.Design.IMenuCommandService?qualifyHint=False> service.  
  
## Changing a menu command label with the IMenuCommandService  
  
1.  Create a VSIX project named `MenuText` with a menu command named **ChangeMenuText**. For more information, see [Creating a VSPackage with a Menu Command](../Topic/Creating%20an%20Extension%20with%20a%20Menu%20Command.md).  
  
2.  In the .vstc file, add the `TextChanges` flag to your menu command, as shown in the following example.  
  
    ```xml  
    <Button guid="guidChangeMenuTextPackageCmdSet" id="ChangeMenuTextId" priority="0x0100" type="Button">  
        <Parent guid="guidChangeMenuTextPackageCmdSet" id="MyMenuGroup" />  
        <Icon guid="guidImages" id="bmpPic1" />  
        <CommandFlag>TextChanges</CommandFlag>  
        <Strings>  
            <ButtonText>Invoke ChangeMenuText</ButtonText>  
        </Strings>  
    </Button>  
    ```  
  
3.  In the ChangeMenuText.cs file, create an event handler that will be called before the menu command is displayed.  
  
    ```c#  
    private void OnBeforeQueryStatus(object sender, EventArgs e)  
    {  
        var myCommand = sender as OleMenuCommand;  
        if (null != myCommand)  
        {  
            myCommand.Text = "New Text";  
                    }  
    }  
    ```  
  
     You can also update the status of the menu command in this method by changing the <xref:System.ComponentModel.Design.MenuCommand.Visible?qualifyHint=False>, <xref:System.ComponentModel.Design.MenuCommand.Checked?qualifyHint=False>, and <xref:System.ComponentModel.Design.MenuCommand.Enabled?qualifyHint=False> properties on the <xref:Microsoft.VisualStudio.Shell.OleMenuCommand?qualifyHint=False> object.  
  
4.  In the ChangeMenuText constructor, replace the original command initialization and placement code with code that creates a <xref:Microsoft.VisualStudio.Shell.OleMenuCommand?qualifyHint=False> (rather than a `MenuCommand`) that represents the menu command, adds the <xref:Microsoft.VisualStudio.Shell.OleMenuCommand.BeforeQueryStatus?qualifyHint=False> event handler, and gives the menu command to the menu command service.  
  
     Here is what it should look like:  
  
    ```c#  
    private ChangeMenuText(Package package)  
    {  
        if (package == null)  
        {  
            throw new ArgumentNullException(nameof(package));  
        }  
  
        this.package = package;  
  
        OleMenuCommandService commandService = this.ServiceProvider.GetService(typeof(IMenuCommandService)) as OleMenuCommandService;  
        if (commandService != null)  
        {  
            CommandID menuCommandID = new CommandID(MenuGroup, CommandId);  
            EventHandler eventHandler = this.ShowMessageBox;  
            OleMenuCommand menuItem = new OleMenuCommand(ShowMessageBox, menuCommandID);  
            menuItem.BeforeQueryStatus +=  
                new EventHandler(OnBeforeQueryStatus);  
            commandService.AddCommand(menuItem);  
        }  
    }  
    ```  
  
5.  Build the project and start debugging. The experimental instance of Visual Studio appears.  
  
6.  On the **Tools** menu you should see a command named **Invoke ChangeMenuText**.  
  
7.  Click the command. You should see the message box announcing that MenuItemCallback has been called. When you dismiss the message box, you should see that the name of the command on the Tools menu is now **New Text**.