---
title: "InitInstance Member Function"
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
ms.assetid: 4ef09267-ff7f-4c39-91a0-57454a264f83
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# InitInstance Member Function
The Windows operating system allows you to run more than one copy, or "instance," of the same application. `WinMain` calls [InitInstance](../vs140/CWinApp--InitInstance.md) every time a new instance of the application starts.  
  
 The standard `InitInstance` implementation created by the MFC Application Wizard performs the following tasks:  
  
-   As its central action, creates the document templates that in turn create documents, views, and frame windows. For a description of this process, see [Document Template Creation](../vs140/Document-Template-Creation.md).  
  
-   Loads standard file options from an .ini file or the Windows registry, including the names of the most recently used files.  
  
-   Registers one or more document templates.  
  
-   For an MDI application, creates a main frame window.  
  
-   Processes the command line to open a document specified on the command line or to open a new, empty document.  
  
 You can add your own initialization code or modify the code written by the wizard.  
  
> [!NOTE]
>  MFC applications must be initialized as single threaded apartment (STA). If you call [CoInitializeEx](http://msdn.microsoft.com/library/windows/desktop/ms695279) in your `InitInstance` override, specify `COINIT_APARTMENTTHREADED` (rather than `COINIT_MULTITHREADED`). For more information, see PRB: MFC Application Stops Responding When You Initialize the Application as a Multithreaded Apartment (828643) at [http://support.microsoft.com/default.aspx?scid=kb;en-us;828643](http://support.microsoft.com/default.aspx?scid=kb;en-us;828643).  
  
## See Also  
 [CWinApp: The Application Class](../vs140/CWinApp--The-Application-Class.md)