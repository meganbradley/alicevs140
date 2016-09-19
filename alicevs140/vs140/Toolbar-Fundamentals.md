---
title: "Toolbar Fundamentals"
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
ms.topic: article
ms.assetid: cc00aaff-8a56-433b-b0c0-b857d76b4ffd
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Toolbar Fundamentals
This article describes the fundamental MFC implementation that lets you add a default toolbar to your application by selecting an option in the Application Wizard. Topics covered include:  
  
-   [The Application Wizard toolbar option](#_core_the_appwizard_toolbar_option)  
  
-   [The toolbar in code](#_core_the_toolbar_in_code)  
  
-   [Editing the toolbar resource](#_core_editing_the_toolbar_resource)  
  
-   [Multiple toolbars](#_core_multiple_toolbars)  
  
##  <a name="_core_the_appwizard_toolbar_option"></a> The Application Wizard Toolbar Option  
 To get a single toolbar with default buttons, select the Standard Docking toolbar option on the page labeled User Interface Features. This adds code to your application that:  
  
-   Creates the toolbar object.  
  
-   Manages the toolbar, including its ability to dock or to float.  
  
##  <a name="_core_the_toolbar_in_code"></a> The Toolbar in Code  
 The toolbar is a [CToolBar](../vs140/CToolBar-Class.md) object declared as a data member of your application's **CMainFrame** class. In other words, the toolbar object is embedded in the main frame window object. This means that MFC creates the toolbar when it creates the frame window and destroys the toolbar when it destroys the frame window. The following partial class declaration, for a multiple document interface (MDI) application, shows data members for an embedded toolbar and an embedded status bar. It also shows the override of the `OnCreate` member function.  
  
 [!CODE [NVC_MFCListView#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCListView#6)]  
  
 Toolbar creation occurs in **CMainFrame::OnCreate**. MFC calls [OnCreate](../vs140/CWnd--OnCreate.md) after creating the window for the frame but before it becomes visible. The default `OnCreate` that the Application Wizard generates does the following toolbar tasks:  
  
1.  Calls the `CToolBar` object's [Create](../vs140/CToolBar--Create.md) member function to create the underlying [CToolBarCtrl](../vs140/CToolBarCtrl-Class.md) object.  
  
2.  Calls [LoadToolBar](../vs140/CToolBar--LoadToolBar.md) to load the toolbar resource information.  
  
3.  Calls functions to enable docking, floating, and tool tips. For details about these calls, see the article [Docking and Floating Toolbars](../vs140/Docking-and-Floating-Toolbars.md).  
  
> [!NOTE]
>  The MFC General sample [DOCKTOOL](../vs140/Visual-C---Samples.md) includes illustrations of both old and new MFC toolbars. The toolbars that use **COldToolbar** require calls in step 2 to `LoadBitmap` (rather than `LoadToolBar`) and to `SetButtons`. The new toolbars require calls to `LoadToolBar`.  
  
 The docking, floating, and tool tips calls are optional. You can remove those lines from `OnCreate` if you prefer. The result is a toolbar that remains fixed, unable to float or redock and unable to display tool tips.  
  
##  <a name="_core_editing_the_toolbar_resource"></a> Editing the Toolbar Resource  
 The default toolbar you get with the Application Wizard is based on an **RT_TOOLBAR** custom resource, introduced in MFC version 4.0. You can edit this resource with the [toolbar editor](../vs140/Toolbar-Editor.md). The editor lets you easily add, delete, and rearrange buttons. It contains a graphical editor for the buttons that is very similar to the general graphics editor in Visual C++. If you edited toolbars in previous versions of Visual C++, you'll find the task much easier now.  
  
 To connect a toolbar button to a command, you give the button a command ID, such as `ID_MYCOMMAND`. Specify the command ID in the button's property page in the toolbar editor. Then create a handler function for the command (see [Mapping Messages to Functions](../vs140/Mapping-Messages-to-Functions.md) for more information).  
  
 New [CToolBar](../vs140/CToolBar-Class.md) member functions work with the **RT_TOOLBAR** resource. [LoadToolBar](../vs140/CToolBar--LoadToolBar.md) now takes the place of [LoadBitmap](../vs140/CToolBar--LoadBitmap.md) to load the bitmap of the toolbar button images, and [SetButtons](../vs140/CToolBar--SetButtons.md) to set the button styles and connect buttons with bitmap images.  
  
 For details about using the toolbar editor, see [Toolbar Editor](../vs140/Toolbar-Editor.md).  
  
##  <a name="_core_multiple_toolbars"></a> Multiple Toolbars  
 The Application Wizard provides you with one default toolbar. If you need more than one toolbar in your application, you can model your code for additional toolbars based on the wizard-generated code for the default toolbar.  
  
 If you want to display a toolbar as the result of a command, you'll need to:  
  
-   Create a new toolbar resource with the toolbar editor and load it in `OnCreate` with the [LoadToolbar](../vs140/CToolBar--LoadToolBar.md) member function.  
  
-   Embed a new [CToolBar](../vs140/CToolBar-Class.md) object in your main frame window class.  
  
-   Make the appropriate function calls in `OnCreate` to dock or float the toolbar, set its styles, and so on.  
  
### What do you want to know more about?  
  
-   [MFC Toolbar Implementation (overview information on toolbars)](../vs140/MFC-Toolbar-Implementation.md)  
  
-   [Docking and floating toolbars](../vs140/Docking-and-Floating-Toolbars.md)  
  
-   [Toolbar tool tips](../vs140/Toolbar-Tool-Tips.md)  
  
-   The [CToolBar](../vs140/CToolBar-Class.md) and [CToolBarCtrl](../vs140/CToolBarCtrl-Class.md) classes  
  
-   [Working with the toolbar control](../vs140/Working-with-the-Toolbar-Control.md)  
  
-   [Using your old toolbars](../vs140/Using-Your-Old-Toolbars.md)  
  
## See Also  
 [MFC Toolbar Implementation](../vs140/MFC-Toolbar-Implementation.md)