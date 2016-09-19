---
title: "Resource Files (C++)"
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
ms.assetid: 338a4a0f-0c62-4ef1-a34f-5d86262d93a4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Resource Files (C++)
Resources are interface elements that provide information to the user. Bitmaps, icons, toolbars, and cursors are all resources. Some resources can be manipulated to perform an action such as selecting from a menu or entering data in dialog box.  
  
 See [Working with Resources](../vs140/Working-with-Resource-Files.md) for more information.  
  
|File name|Directory location|Solution Explorer location|Description|  
|---------------|------------------------|--------------------------------|-----------------|  
|*Projname*.rc|*Projname*|Source Files|The resource script file for the project. The resource script file contains the following, depending on the type of project, and the support selected for the project (for example, toolbars, dialog boxes, or HTML):<br /><br /> -   Default menu definition.<br />-   Accelerator and string tables.<br />-   Default **About** dialog box.<br />-   Other dialog boxes.<br />-   Icon file (res\\*Projname*.ico).<br />-   Version information.<br />-   Bitmaps.<br />-   Toolbar.<br />-   HTML files.<br /><br /> The resource file includes the file Afxres.rc for standard Microsoft Foundation Class resources.|  
|Resource.h|*Projname*|Header Files|The resource header file that includes definitions for the resources used by the project.|  
|*Projname*.rc2|*Projname*\res|Source Files|The script file containing additional resources used by the project. You can include the .rc2 file at the top of the project's .rc file.<br /><br /> An .rc2 file is useful for including resources used by several different projects. Instead of having to create the same resources several times for different projects, you can put them in an .rc2 file and include the .rc2 file into the main .rc file.|  
|*Projname*.def|*Projname*|Source Files|The module definition file for a DLL project. For a control, it provides the name and description of the control, as well as the size of the run-time heap.|  
|*Projname*.ico|*Projname*\res|Resource Files|The icon file for the project or control. This icon appears when the application is minimized. It is also used in the application's **About** box. By default, MFC provides the MFC icon, and ATL provides the ATL icon.|  
|*Projname*Doc.ico|*Projname*\res|Resource Files|The icon file for an MFC project that includes support for the document/view architecture.|  
|Toolbar.bmp|*Projname*\res|Resource Files|The bitmap file representing the application or control in a toolbar or palette. This bitmap is included in the project's resource file. The initial toolbar and status bar are constructed in the **CMainFrame** class.|  
|ribbon.mfcribbon-ms|*Projname*\res|Resource Files|The resource file that contains the XML code that defines the buttons, controls, and attributes in the ribbon. For more information, see [Ribbon Designer (MFC)](../vs140/Ribbon-Designer--MFC-.md).|  
  
## See Also  
 [File Types Created for Visual C++ Projects](../vs140/File-Types-Created-for-Visual-C---Projects.md)