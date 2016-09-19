---
title: "MFC Program or Control Source and Header Files"
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
ms.assetid: f61419a8-bf69-4bbb-8f7c-1734be5e6db6
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC Program or Control Source and Header Files
The following files are created when you create an MFC project in Visual Studio, depending on the options you select for the project you create. For example, your project contains *Projname*dlg.cpp and *Projname*dlg.h files only if you create a dialog-based project or class.  
  
 All of these files are located in the *Projname* directory, and in either the Header Files (.h files) folder or Source Files (.cpp files) folder in Solution Explorer.  
  
|File name|Description|  
|---------------|-----------------|  
|*Projname*.h|The main include file for the program or DLL. It contains all global symbols and `#include` directives for other header files. It derives the `CPrjnameApp` class from `CWinApp` and declares an `InitInstance` member function. For a control, the `CPrjnameApp` class is derived from `COleControlModule`.|  
|*Projname*.cpp|The main program source file. It creates one object of the class `CPrjnameApp`, which is derived from `CWinApp`, and overrides the `InitInstance` member function.<br /><br /> For executables, `CPrjnameApp::InitInstance` does several things. It registers document templates, which serve as a connection between documents and views; creates a main frame window; and creates an empty document (or opens a document if one is specified as a command-line argument to the application).<br /><br /> For DLLs and ActiveX (formerly OLE) controls, `CProjNameApp::InitInstance` registers the control's object factory with OLE by calling `COleObjectFactory::RegisterAll` and makes a call to `AfxOLEInit`. In addition, the member function `CProjNameApp::ExitInstance` is used to unload the control from memory with a call to **AfxOleTerm**.<br /><br /> This file also registers and unregisters the control in the Windows registration database by implementing the `DllRegisterServer` and `DllUnregisterServer` functions.|  
|*Projname*ctrl.h, *Projname*ctrl.cpp|Declare and implement the `CProjnameCtrl` class. `CProjnameCtrl` is derived from `COleControl`, and skeleton implementations of some member functions are defined that initialize, draw, and serialize (load and save) the control. Message, event, and dispatch maps are also defined.|  
|*Projname*dlg.cpp, *Projname*dlg.h|Created if you choose a dialog-based application. The files derive and implement the dialog class, named `CProjnameDlg`, and include skeleton member functions to initialize a dialog and perform dialog data exchange (DDX). Your About dialog class is also placed in these files instead of in *Projname*.cpp.|  
|Dlgproxy.cpp, Dlgproxy.h|In a dialog-based program, the implementation and header file for the project's Automation proxy class for the main dialog. This is only used if you have chosen Automation support.|  
|*Projname*doc.cpp, *Projname*doc.h|Derive and implement the document class, named `CProjnameDoc`, and include skeleton member functions to initialize a document, serialize (save and load) a document, and implement debugging diagnostics.|  
|*Projname*set.h/.cpp|Created if you create a program that supports a database and contains the recordset class.|  
|*Projname*view.cpp, *Projname*view.h|Derive and implement the view class, named `CProjnameView`, which is used to display and print the document data. The `CProjnameView` class is derived from one of the following MFC classes:<br /><br /> -   [CEditView](../vs140/CEditView-Class.md)<br />-   [CFormView](../vs140/CFormView-Class.md)<br />-   [CRecordView](../vs140/CRecordView-Class.md)<br />-   [COleDBRecordView](../vs140/COleDBRecordView-Class.md)<br />-   [CTreeView](../vs140/CTreeView-Class.md)<br />-   [CListView](../vs140/CListView-Class.md)<br />-   [CRichEditView](../vs140/CRichEditView-Class.md)<br />-   [CScrollView](../vs140/CScrollView-Class.md)<br />-   [CView](../vs140/CView-Class.md)<br />-   [CHTMLView](../vs140/CHtmlView-Class.md)<br />-   [CHTMLEditView](../vs140/CHtmlEditView-Class.md)<br /><br /> The project's view class contains skeleton member functions to draw the view and implement debugging diagnostics. If you have enabled support for printing, then message-map entries are added for print, print setup, and print preview command messages. These entries call the corresponding member functions in the base view class.|  
|*Projname*PropPage.h, *Projname*PropPage.cpp|Declare and implement the `CProjnamePropPage` class. `CProjnamePropPage` is derived from `COlePropertyPage` and a skeleton member function, `DoDataExchange`, is provided to implement data exchange and validation.|  
|IPframe.cpp, IPframe.h|Created if the Mini-Server or Full-Server option is selected in the application wizard's **Automation Options** page (step 3 of 6). The files derive and implement the in-place frame window class, named **CInPlaceFrame**, used when the server is in place activated by a container program.|  
|Mainfrm.cpp, Mainfrm.h|Derive the **CMainFrame** class from either [CFrameWnd](../vs140/CFrameWnd-Class.md) (for SDI applications) or [CMDIFrameWnd](../vs140/CMDIFrameWnd-Class.md) (for MDI applications). The **CMainFrame** class handles the creation of toolbar buttons and the status bar, if the corresponding options are selected in the application wizard's **Application Options** page (step 4 of 6). For information on using **CMainFrame**, see [The Frame-Window Classes Created by the Application Wizard](../vs140/Frame-Window-Classes-Created-by-the-Application-Wizard.md).|  
|Childfrm.cpp, Childfrm.h|Derive the **CChildFrame** class from [CMDIChildWnd](../vs140/CMDIChildWnd-Class.md). The **CChildFrame** class is used for MDI document frame windows. These files are always created if you select the MDI option.|  
  
## See Also  
 [File Types Created for Visual C++ Projects](../vs140/File-Types-Created-for-Visual-C---Projects.md)   
 [ATL Program or Control Source and Header Files](../vs140/ATL-Program-or-Control-Source-and-Header-Files.md)   
 [CLR Projects](../vs140/Files-Created-for-CLR-Projects.md)