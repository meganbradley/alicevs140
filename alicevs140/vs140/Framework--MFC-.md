---
title: "Framework (MFC)"
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
ms.assetid: 3be0fec8-9843-4119-ae42-ece993ef500b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Framework (MFC)
Your work with the Microsoft Foundation Class (MFC) Library framework is based largely on a few major classes and several Visual C++ tools. Some classes encapsulate a large portion of the Win32 application programming interface (API). Other classes encapsulate application concepts such as documents, views, and the application itself. Still others encapsulate OLE features and ODBC and DAO data-access functionality.  
  
 For example, Win32's concept of window is encapsulated by MFC class `CWnd`. That is, a C++ class called `CWnd` encapsulates or "wraps" the `HWND` handle that represents a Windows window. Likewise, class `CDialog` encapsulates Win32 dialog boxes.  
  
 Encapsulation means that the C++ class `CWnd`, for example, contains a member variable of type `HWND`, and the class's member functions encapsulate calls to Win32 functions that take an `HWND` as a parameter. The class member functions typically have the same name as the Win32 function they encapsulate.  
  
## In This Section  
 [SDI and MDI](../vs140/SDI-and-MDI.md)  
  
 [Documents, Views, and the Framework](../vs140/Documents--Views--and-the-Framework.md)  
  
 [Wizards and Resource Editors](../vs140/Wizards-and-the-Resource-Editors.md)  
  
## In Related Sections  
 [Building on the Framework](../vs140/Building-on-the-Framework.md)  
  
 [How the Framework Calls Your Code](../vs140/How-the-Framework-Calls-Your-Code.md)  
  
 [CWinApp: The Application Class](../vs140/CWinApp--The-Application-Class.md)  
  
 [Document Templates and the Document/View Creation Process](../vs140/Document-Templates-and-the-Document-View-Creation-Process.md)  
  
 [Message Handling and Mapping](../vs140/Message-Handling-and-Mapping.md)  
  
 [Window Objects](../vs140/Window-Objects.md)  
  
## See Also  
 [Using the Classes to Write Applications for Windows](../vs140/Using-the-Classes-to-Write-Applications-for-Windows.md)