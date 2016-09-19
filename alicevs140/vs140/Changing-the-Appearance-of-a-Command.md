---
title: "Changing the Appearance of a Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: da2474fa-f92d-4e9e-b8bf-67c61bf249c2
caps.latest.revision: 25
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Changing the Appearance of a Command
You can provide feedback to your user by changing the appearance of a command. For example, you may want a command to look different when it is unavailable. You can make commands available or unavailable, hide or show them, or check or uncheck them on the menu.  
  
 To change the appearance of a command, perform one of these actions:  
  
-   Specify the appropriate flags in the command definition in the command table file.  
  
-   Use the <xref:Microsoft.VisualStudio.Shell.OleMenuCommandService?qualifyHint=False> service.  
  
-   Implement the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget?qualifyHint=False> interface and modify the raw command objects.  
  
 The following steps show how to find and update the appearance of a command by using the Managed Package Framework (MPF).  
  
### To change the appearance of a menu command  
  
1.  Follow the instructions in [How to: Change the Text of a Menu Command](../vs140/Changing-the-Text-of-a-Menu-Command.md) to create a menu item named `New Text`.  
  
2.  In the ChangeMenuText.cs file, add the following using statement:  
  
    ```c#  
    using System.Security.Permissions;  
    ```  
  
3.  In the ChangeMenuTextPackageGuids.cs file, add the following line:  
  
    ```c#  
    public const string guidChangeMenuTextPackageCmdSet= "00000000-0000-0000-0000-00000000";  // get the GUID from the .vsct file  
    ```  
  
4.  In the ChangeMenuText.cs file, replace the code in the ShowMessageBox method with the following:  
  
    ```c#  
    private void ShowMessageBox(object sender, EventArgs e)  
    {  
        var command = sender as OleMenuCommand;  
        if (command.Text == "New Text")  
            ChangeMyCommand(command.CommandID.ID, false);}  
    }  
    ```  
  
5.  Obtain the command that you want to update from the <xref:Microsoft.VisualStudio.Shell.OleMenuCommandService?qualifyHint=False> object and then set the appropriate properties on the command object. For example, the following method makes the specified command from a VSPackage command set available or unavailable. The following code makes the menu item named `New Text` unavailable after it has been clicked.  
  
    ```c#  
    public bool ChangeMyCommand(int cmdID, bool enableCmd)  
    {  
        bool cmdUpdated = false;  
        var mcs = this.ServiceProvider.GetService(typeof(IMenuCommandService))  
            as OleMenuCommandService;  
        var newCmdID = new CommandID(new Guid(ChangeMenuTextPackageGuids.guidChangeMenuTextPackageCmdSet), cmdID);  
        MenuCommand mc = mcs.FindCommand(newCmdID);  
        if (mc != null)  
        {  
            mc.Enabled = enableCmd;  
            cmdUpdated = true;  
        }  
        return cmdUpdated;    }  
    }  
    ```  
  
6.  Build the project and start debugging. The experimental instance of Visual Studio should appear.  
  
7.  On the **Tools** menu, click the **Invoke ChangeMenuText** command. At this point the command name is **Invoke ChangeMenuText**, so the command handler doesn’t call ChangeMyCommand().  
  
8.  On the **Tools** menu you should now see **New Text**. Click **New Text**. The command should now be grayed out.  
  
## See Also  
 [Menu and Toolbar Commands](../Topic/Commands,%20Menus,%20and%20Toolbars.md)   
 [How VSPackages Contribute User Interface Elements](../Topic/How%20VSPackages%20Add%20User%20Interface%20Elements.md)   
 [Common Menu Tasks](../vs140/Extending-Menus-and-Commands.md)   
 [XML-Based Command Table Configuration (.vsct) Files](../vs140/Visual-Studio-Command-Table--.Vsct--Files.md)