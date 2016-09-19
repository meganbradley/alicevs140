---
title: "How to: Use Resource Templates"
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
ms.assetid: bdfe7060-f98e-4859-8285-9c8570360e9d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use Resource Templates
A resource template is a customized resource that you have saved as an .rct file. A resource template can then serve as a starting point for creating other resources. Resource templates save time in developing additional resources or groups of resources that share features, such as standard controls and other repeated elements. For example, you might want to include a Help button and an icon of a company logo in several dialog boxes. To do so quickly, create a new dialog box template and customize it with the logo and the Help button.  
  
 Once you have customized the resource template, you must save your changes in the template folder (or any location specified in the include path) so that the new resource template will appear under its resource type in the [Add Resource dialog box](../vs140/Add-Resource-Dialog-Box.md). You can then use the new resource template as often as needed.  
  
> [!NOTE]
>  You can place language-specific template files in subdirectories of the main template directory. For example, you can place English-only template files in \\<resource template directory\>\1033.  
  
### To create a template for resources  
  
1.  In **Solution Explorer**, right-click your project.  
  
2.  From the shortcut menu, choose **Add**, then click **Add New Item**.  
  
3.  In the **Add New Item** dialog box, in the **Templates:** pane, choose **Resource Template File (.rct)**.  
  
4.  Provide a name and location for your new .rct file and click **Open**.  
  
5.  The new .rct file is added to your project and appears in Solution Explorer under the **Resources** folder.  
  
     You can now double-click the .rct file to open it in a document window, then add resources to it (right-click the file in the document window and choose **Add Resource** from the shortcut menu). You can then customize those resources and save the .rct file.  
  
    > [!NOTE]
    >  When you create a new RCT file, Visual Studio searches for it in \Program Files\Microsoft Visual Studio 9.0\VC\VCResourceTemplates, in \Program Files\Microsoft Visual Studio 9.0\VC\VCResourceTemplates\\*LCID* (such as 1033 for English), *or* anywhere on the [include path](../vs140/How-to--Specify-Include-Directories-for-Resources.md). If you prefer to store your RCT files in another file folder, for example \My Documents, you only need to add this folder to the include path and Visual Studio will find your RCT file.  
  
### To convert an existing .rc file to an .rct file  
  
1.  [Open the .rc file as a stand-alone file](../vs140/How-to--Open-a-Resource-Script-File-Outside-of-a-Project--Standalone-.md).  
  
2.  On the **File** menu, click **Save <*your filename*> As**.  
  
3.  Specify a location and click **OK**.  
  
### To create a new resource from a template  
  
1.  In the [Resource View](../vs140/Resource-View-Window.md) pane, right click the .rc file and choose **Add Resource** from the shortcut menu.  
  
2.  In the **Add Resource** dialog box, click the plus sign (**+**) next to a resource to expand the resource node and see all the templates available for that resource.  
  
3.  Double-click the template you want to use.  
  
4.  Modify the added resource as needed in its resource editor.  
  
     The resource editor automatically provides a unique resource ID. You can revise the [resource properties](../vs140/Changing-the-Properties-of-a-Resource.md) as needed.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.*  
  
 Requirements  
  
 Win32  
  
## See Also  
 [Resource Files](../vs140/Resource-Files--Visual-Studio-.md)   
 [Resource Editors](../vs140/Resource-Editors.md)