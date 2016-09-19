---
title: "Frame-Window Classes Created by the Application Wizard"
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
ms.assetid: 9947df73-4470-49a0-ac61-7b6ee401a74e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Frame-Window Classes Created by the Application Wizard
When you use the [Application Wizard](../vs140/Creating-Desktop-Projects-By-Using-Application-Wizards.md) to create a skeleton application, in addition to application, document, and view classes, the Application Wizard creates a derived frame-window class for your application's main frame window. The class is called `CMainFrame` by default, and the files that contain it are named MAINFRM.H and MAINFRM.CPP.  
  
 If your application is SDI, your `CMainFrame` class is derived from class [CFrameWnd](../vs140/CFrameWnd-Class.md).  
  
 If your application is MDI, `CMainFrame` is derived from class [CMDIFrameWnd](../vs140/CMDIFrameWnd-Class.md). In this case `CMainFrame` implements the main frame, which holds the menu, toolbar, and status bars. The Application Wizard does not derive a new document frame-window class for you. Instead, it uses the default implementation in [CMDIChildWnd Class](../vs140/CMDIChildWnd-Class.md). The MFC framework creates a child window to contain each view (which can be of type `CScrollView`, `CEditView`, `CTreeView`, `CListView`, and so on) that the application requires. If you need to customize your document frame window, you can create a new document frame-window class (see [Adding a Class](../vs140/Adding-a-Class--Visual-C---.md)).  
  
 If you choose to support a toolbar, the class also has member variables of type [CToolBar](../vs140/CToolBar-Class.md) and [CStatusBar](../vs140/CStatusBar-Class.md) and an `OnCreate` message-handler function to initialize the two [control bars](../vs140/Control-Bars.md).  
  
 These frame-window classes work as created, but to enhance their functionality, you must add member variables and member functions. You may also want to have your window classes handle other Windows messages. For more information, see [Changing the Styles of a Window Created by MFC](../vs140/Changing-the-Styles-of-a-Window-Created-by-MFC.md).  
  
## See Also  
 [Frame-Window Classes](../vs140/Frame-Window-Classes.md)   
 [MFC Program or Control Source and Header Files](../vs140/MFC-Program-or-Control-Source-and-Header-Files.md)