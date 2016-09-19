---
title: "Hosting a Windows Forms User Control as an MFC View"
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
ms.assetid: 43c02ab4-1366-434c-a980-0b19326d6ea0
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Hosting a Windows Forms User Control as an MFC View
MFC uses the CWinFormsView class to host a Windows Forms user control in an MFC view. MFC Windows Forms views are ActiveX controls. The user control is hosted as a child of the native view and occupies the entire client area of the native view.  
  
 The end result resembles the model used by the [CFormView Class](../vs140/CFormView-Class.md). This lets you take advantage of the Windows Forms designer and runtime to create rich form-based views.  
  
 Because MFC Windows Forms views are ActiveX controls, they do not have the same `hwnd` as MFC views. Also they cannot be passed as a pointer to a [CView](../vs140/CView-Class.md) view. In general, use .NET Framework methods to work with Windows Forms views and rely less on Win32.  
  
 For a sample application that shows Windows Forms used with MFC, see [MFC and Windows Forms Integration](http://www.microsoft.com/downloads/details.aspx?FamilyID=987021bc-e575-4fe3-baa9-15aa50b0f599&displaylang=en).  
  
## In This Section  
 [How to: Create the User Control and Host MDI View](../vs140/How-to--Create-the-User-Control-and-Host-MDI-View.md)  
  
 [How to: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md)  
  
 [How to: Call Properties and Methods of the Windows Forms Control](../vs140/How-to--Call-Properties-and-Methods-of-the-Windows-Forms-Control.md)  
  
## See Also  
 [Using Windows Forms in MFC](../vs140/Using-a-Windows-Form-User-Control-in-MFC.md)   
 [How to: Author User Controls](assetId:///79c9cf05-5ab6-4a18-886d-88a64748b098)