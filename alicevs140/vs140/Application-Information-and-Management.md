---
title: "Application Information and Management"
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
ms.assetid: b72f4154-24db-4e75-bca3-6873e2459c15
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Application Information and Management
When you write an application, you create a single [CWinApp](../vs140/CWinApp-Class.md)-derived object. At times, you may want to get information about this object from outside the `CWinApp`-derived object.  
  
 The Microsoft Foundation Class Library provides the following global functions to help you accomplish these tasks:  
  
### Application Information and Management Functions  
  
|||  
|-|-|  
|[AfxBeginThread](../vs140/AfxBeginThread.md)|Creates a new thread.|  
|[AfxEndThread](../vs140/AfxEndThread.md)|Terminates the current thread.|  
|[AfxFreeLibrary](../vs140/AfxFreeLibrary.md)|Decrements the reference count of the loaded dynamic-link library (DLL) module; when the reference count reaches zero, the module is unmapped.|  
|[AfxGetApp](../vs140/AfxGetApp.md)|Returns a pointer to the application's single `CWinApp` object.|  
|[AfxGetAppName](../vs140/AfxGetAppName.md)|Returns a string that contains the application's name.|  
|[AfxGetInstanceHandle](../vs140/AfxGetInstanceHandle.md)|Returns an `HINSTANCE` representing this instance of the application.|  
|[AfxGetMainWnd](../vs140/AfxGetMainWnd.md)|Returns a pointer to the current "main" window of a non-OLE application, or the in-place frame window of a server application.|  
|[AfxGetPerUserRegistration](../vs140/AfxGetPerUserRegistration.md)|Use this function to determine whether the application redirects registry access to the **HKEY_CURRENT_USER** (**HKCU**) node.|  
|[AfxGetResourceHandle](../vs140/AfxGetResourceHandle.md)|Returns an `HINSTANCE` to the source of the application's default resources. Use this to access the application's resources directly.|  
|[AfxGetThread](../vs140/AfxGetThread.md)|Retrieves a pointer to the current [CWinThread](../vs140/CWinThread-Class.md) object.|  
|[AfxInitRichEdit](../vs140/AfxInitRichEdit.md)|Initializes the version 1.0 rich edit control for the application.|  
|[AfxInitRichEdit2](../vs140/AfxInitRichEdit2.md)|Initializes the version 2.0 and later rich edit control for the application.|  
|[AfxLoadLibrary](../vs140/AfxLoadLibrary.md)|Maps a DLL module and returns a handle that can be used to obtain the address of a DLL function.|  
|[AfxRegisterClass](../vs140/AfxRegisterClass.md)|Registers a window class in a DLL that uses MFC.|  
|[AfxRegisterWndClass](../vs140/AfxRegisterWndClass.md)|Registers a Windows window class to supplement those registered automatically by MFC.|  
|[AfxSetPerUserRegistration](../vs140/AfxSetPerUserRegistration.md)|Sets whether the application redirects registry access to the **HKEY_CURRENT_USER** (**HKCU**) node.|  
|[AfxSetResourceHandle](../vs140/AfxSetResourceHandle.md)|Sets the `HINSTANCE` handle where the default resources of the application are loaded.|  
|[AfxSocketInit](../vs140/AfxSocketInit.md)|Called in a `CWinApp::InitInstance` override to initialize Windows Sockets.|  
|[AfxWinInit](../vs140/AfxWinInit.md)|Called by the MFC-supplied `WinMain` function, as part of the [CWinApp](../vs140/CWinApp-Class.md) initialization of a GUI-based application, to initialize MFC. Must be called directly for console applications that use MFC.|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CWinApp Class](../vs140/CWinApp-Class.md)