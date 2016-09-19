---
title: "Application Type, MFC Application Wizard"
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
ms.assetid: c3f62b0e-3f13-42c5-9859-d3890d0c3e1d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Application Type, MFC Application Wizard
Use this page of the [MFC Application Wizard](../vs140/MFC-Application-Wizard.md) to design and add basic features to a new MFC application.  
  
 **Application type**  
 Specifies the type of document support that you want to create in your application. The type of application you select determines the user interface options that are available for your application. See [User Interface Features, MFC Application Wizard](../vs140/User-Interface-Features--MFC-Application-Wizard.md) for more information.  
  
 For more information about the types of documents, see:  
  
-   [SDI and MDI](../vs140/SDI-and-MDI.md)  
  
-   [Frame Windows](../vs140/Frame-Windows.md)  
  
-   [Frame-Window Classes](../vs140/Frame-Window-Classes.md)  
  
-   [Documents, Views, and the Framework](../vs140/Documents--Views--and-the-Framework.md)  
  
-   [Dialog Boxes](../vs140/Dialog-Boxes.md)  
  
|Option|Description|  
|------------|-----------------|  
|**Single document**|Creates a single document interface (SDI) architecture for your application, where a view class is based on [CView Class](../vs140/CView-Class.md). You can change the base class for the view in the [Generated Classes, MFC Application Wizard](../vs140/Generated-Classes--MFC-Application-Wizard.md) page of the wizard. To create a form-based application, for example, use [CFormView Class](../vs140/CFormView-Class.md) for the view class.<br /><br /> In this type of application, the document's frame window can hold only one document.|  
|**Multiple documents**|Creates a multiple document interface (MDI) architecture for your application, where a view class is based on `CView`. You can change the base class for the view in the **Generated Classes** page of the wizard. To create a form-based application, for example, use `CFormView` for the view class.<br /><br /> In this type of application, the document's frame window can hold multiple child windows.|  
|**Tabbed documents**|Places each document on a separate tab.|  
|**Dialog based**|Creates a dialog-based architecture for your application where a dialog class is based on `CDialog`. (To create an HTML dialog, select the box **Use HTML dialog**.)|  
|**Use HTML dialog**|For dialog box applications only. Derives the dialog class from [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md) instead of [CDialog Class](../vs140/CDialog-Class.md). If you check this box, `CDHtmlDialog` is listed in the **Base class** box in the [Generated Classes, MFC Application Wizard](../vs140/Generated-Classes--MFC-Application-Wizard.md) page of the wizard.<br /><br /> A `CDHtmlDialog`-derived dialog box displays HTML-based dialog boxes, exchanges data with HTML controls and handles HTML events.|  
|**Multiple top-level documents**|Creates a multiple top-level architecture for your application, where a view class is based on `CView`.<br /><br /> In this type of application, when a user clicks **New** (or **New Frame**) on the **File** menu, the application creates a window whose parent is implicitly the desktop. The new document frame appears in the taskbar and is not restricted to the client area of the application window.|  
  
 **Document/view architecture support**  
 Specifies whether to include document/view architecture in your application by using the [CDocument Class](../vs140/CDocument-Class.md) and the [CView Class](../vs140/CView-Class.md) (default). Clear this check box if you are porting a non-MFC application or if you want to reduce the size of your compiled executable. By default, an application without document/view architecture is derived from [CWinApp Class](../vs140/CWinApp-Class.md), and it does not include MFC support for opening a document from a disk file.  
  
 **Resource language**  
 Sets the language of your resources. The list displays the languages available on your system, as installed by Visual Studio. If you want to select a language other than your system language, the appropriate template folder for that language must already be installed. For more information about installing language resources different from the defaults available in the **Resource language** list, see [Wizard Support for Other Languages](../vs140/Wizard-Support-for-Other-Languages.md).  
  
 The language that you select is reflected in the **Localized strings** option of the [Document Template Strings, MFC Application Wizard](../vs140/Document-Template-Strings--MFC-Application-Wizard.md) page of the wizard.  
  
 **Use Unicode libraries**  
 Specifies whether the Unicode or non-Unicode version of the MFC libraries is used.  
  
 **Project style**  
 Indicates whether your application has a standard MFC, File Explorer, Visual Studio, or Office architecture and display. For more information, see [Creating a Windows Explorer-Style MFC Application](../vs140/Creating-a-File-Explorer-Style-MFC-Application.md).  
  
|Option|Description|  
|------------|-----------------|  
|**MFC standard**|Provides a standard MFC application architecture.|  
|**File Explorer**|Implements a File Explorer–like application by using a splitter window where the left pane is a [CTreeView Class](../vs140/CTreeView-Class.md) and the right pane is a [CListView Class](../vs140/CListView-Class.md).|  
|**Visual Studio**|Implements a Visual Studio–like application that contains four dockable panes (**File View**, **Class View**, **Properties**, and **Output**) that are derived from [CDockablePane Class](../vs140/CDockablePane-Class.md) and a main frame window that is derived from [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md) (default).|  
|**Office**|Implements an Office–like application that contains a ribbon that is derived from [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md), an Outlook bar that is derived from [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md), a caption bar that is derived from [CMFCCaptionBar Class](../vs140/CMFCCaptionBar-Class.md), and a main frame that is derived from [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md).|  
  
 **Visual style and colors**  
 Determines the visual style of the application. The following options are available:  
  
-   **Windows Native/Default**  
  
-   **Office 2003**  
  
-   **Visual Studio 2005**  
  
-   **Office 2007 (Blue theme)**  
  
-   **Office 2007 (Black theme)**  
  
-   **Office 2007 (Silver theme)**  
  
-   **Office 2007 (Aqua theme)**  
  
 **Enable visual style switching**  
 Specifies whether the user can change the visual style of the application at runtime, usually by selecting the appropriate visual style from a menu or ribbon.  
  
 **Use of MFC**  
 Specifies how to link to the MFC library. By default, MFC is linked as a shared DLL.  
  
|Option|Description|  
|------------|-----------------|  
|**Use MFC in a shared DLL**|Links the MFC library to an application as a shared DLL. The application makes calls to the MFC library at run time. This option reduces the disk and memory requirements of applications that consist of multiple executable files that use the MFC library. Both Win32 and MFC applications can call functions in your DLL (default)|  
|**Use MFC in a static library**|Links an application to the static MFC library at build time.|  
  
## See Also  
 [MFC Application Wizard](../vs140/MFC-Application-Wizard.md)   
 [File Types Created for Visual C++ Projects](../vs140/File-Types-Created-for-Visual-C---Projects.md)