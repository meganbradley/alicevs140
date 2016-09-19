---
title: "How to: Add Command Routing to the Windows Forms Control"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: bf138ece-b463-442a-b0a0-de7063a760c0
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Add Command Routing to the Windows Forms Control
[CWinFormsView](../Topic/CWinFormsView%20Class.md) routes commands and update-command UI messages to the user control to allow it to handle MFC commands (for example, frame menu items and toolbar buttons).  
  
 The user control uses [ICommandTarget::Initialize](../vs140/ICommandTarget--Initialize.md) to store a reference to the command source object in `m_CmdSrc`, as shown in the following example. To use `ICommandTarget` you must add a reference to mfcmifc80.dll.  
  
 `CWinFormsView` handles several of the common MFC view notifications by forwarding them to the managed user control. These notifications include the [OnInitialUpdate](../vs140/IView--OnInitialUpdate.md), [OnUpdate](../vs140/IView--OnUpdate.md) and [OnActivateView](../vs140/IView--OnActivateView.md) methods of the [IView Interface](../vs140/IView-Interface.md).  
  
 This topic assumes you have previously completed [How to: Create the User Control and Host in a Dialog Box](../vs140/How-to--Create-the-User-Control-and-Host-in-a-Dialog-Box.md) and [How to: Create the User Control and Host MDI View](../vs140/How-to--Create-the-User-Control-and-Host-MDI-View.md).  
  
### To create the MFC host application  
  
1.  Open Windows Forms Control Library you created in [How to: Create the User Control and Host in a Dialog Box](../vs140/How-to--Create-the-User-Control-and-Host-in-a-Dialog-Box.md).  
  
2.  Add a reference to mfcmifc80.dll, which you can do by right-clicking the project node in **Solution Explorer**, selecting **Add**, **Reference**, and then browsing to Microsoft Visual Studio 10.0\VC\atlmfc\lib.  
  
3.  Open UserControl1.Designer.cs and add the following using statement:  
  
    ```  
    using Microsoft.VisualC.MFC;  
    ```  
  
4.  Also, in UserControl1.Designer.cs, change this line:  
  
    ```  
    partial class UserControl1  
    ```  
  
     to this:  
  
    ```  
    partial class UserControl1 : System.Windows.Forms.UserControl, ICommandTarget  
    ```  
  
5.  Add this as the first line of the class definition for `UserControl1`:  
  
    ```  
    private ICommandSource m_CmdSrc;  
    ```  
  
6.  Add the following method definitions to `UserControl1` (we will create the ID of the MFC control in the next step):  
  
    ```  
    public void Initialize (ICommandSource cmdSrc)  
    {  
       m_CmdSrc = cmdSrc;  
       // need ID of control in MFC dialog and callback function   
       m_CmdSrc.AddCommandHandler(32771, new CommandHandler (singleMenuHandler));  
    }  
  
    private void singleMenuHandler (uint cmdUI)  
    {  
       // User command handler code  
       System.Windows.Forms.MessageBox.Show("Custom menu option was clicked.");  
    }  
    ```  
  
7.  Open the MFC application you created in [How to: Create the User Control and Host MDI View](../vs140/How-to--Create-the-User-Control-and-Host-MDI-View.md).  
  
8.  Add a menu option that will invoke `singleMenuHandler`.  
  
     Go to **Resource View** (Ctrl+Shift+E), expand the **Menu** folder, and then double-click **IDR_MFC02TYPE**. This displays the menu editor.  
  
     Add a menu option at the bottom of the **View** menu. Notice the ID of the menu option in the **Properties** window. Save the file.  
  
     In **Solution Explorer**, open the Resource.h file, copy the ID value for the menu option you just added, and paste that value as the first parameter to the `m_CmdSrc.AddCommandHandler` call in the C# project's `Initialize` method (replacing `32771` if necessary).  
  
9. Build and run the project.  
  
     On the **Build** menu, click **Build Solution**.  
  
     On the **Debug** menu, click **Start without debugging**.  
  
     Select the menu option you added. Notice that the method in the .dll is called.  
  
## See Also  
 [Hosting a Windows Forms User Control as an MFC View](../vs140/Hosting-a-Windows-Forms-User-Control-as-an-MFC-View.md)   
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)   
 [ICommandTarget Interface](../vs140/ICommandTarget-Interface.md)   
 [CommandHandler Delegate](../vs140/CommandHandler-Delegate.md)