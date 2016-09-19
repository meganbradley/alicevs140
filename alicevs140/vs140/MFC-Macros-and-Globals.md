---
title: "MFC Macros and Globals"
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
ms.assetid: add4e33f-0e62-4d27-be14-896cb8675d22
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC Macros and Globals
The Microsoft Foundation Class Library can be divided into two major sections: (1) the MFC classes and (2) macros and globals. If a function or variable is not a member of a class, it is a global function or variable.  
  
 The MFC library and the Active Template Library (ATL) share string conversion macros. For more information, see [String Conversion Macros](../vs140/String-Conversion-Macros.md) in the ATL documentation.  
  
 The MFC macros and globals offer functionality in the following categories.  
  
## General MFC  
  
-   [Data types](../vs140/Data-Types--MFC-.md)  
  
-   [Type casting of MFC class objects](../vs140/Type-Casting-of-MFC-Class-Objects.md)  
  
-   [Run-time object model services](../vs140/Run-Time-Object-Model-Services.md)  
  
-   [Diagnostic services](../vs140/Diagnostic-Services.md)  
  
-   [Exception processing](../vs140/Exception-Processing.md)  
  
-   [CString formatting and message-box display](../vs140/CString-Formatting-and-Message-Box-Display.md)  
  
-   [Message maps](../vs140/Message-Map-Macros--MFC-.md)  
  
-   [Application information and management](../vs140/Application-Information-and-Management.md)  
  
-   [Standard command and window IDs](../vs140/Standard-Command-and-Window-IDs.md)  
  
-   [Collection class helpers](../vs140/Collection-Class-Helpers.md)  
  
-   [Gray and dithered bitmap functions](../vs140/Gray-and-Dithered-Bitmap-Functions.md)  
  
-   [Standard dialog data exchange (DDX) routines](../vs140/Standard-Dialog-Data-Exchange-Routines.md)  
  
-   [Standard dialog data validation (DDV) routines](../vs140/Standard-Dialog-Data-Validation-Routines.md)  
  
-   [AFX Messages](../vs140/AFX-Messages.md)  
  
-   [Toolbar Control Styles](../vs140/ToolBar-Control-Styles.md)  
  
-   [CMFCImagePaintArea::IMAGE_EDIT_MODE Enumeration](../vs140/CMFCImagePaintArea--IMAGE_EDIT_MODE-Enumeration.md)  
  
## Database  
  
-   [Record Field Exchange (RFX) functions](../vs140/Record-Field-Exchange-Functions.md) and [Bulk Record Field Exchange (bulk RFX) functions](../vs140/Record-Field-Exchange-Functions.md) for the MFC ODBC classes  
  
-   [Record field exchange (DFX) functions](../vs140/Record-Field-Exchange-Functions.md) for the MFC DAO classes  
  
-   [Dialog data exchange (DDX) functions for CRecordView and CDaoRecordView](../vs140/Dialog-Data-Exchange-Functions-for-CRecordView-and-CDaoRecordView.md) (MFC ODBC and DAO classes)  
  
-   [Dialog data exchange (DDX) functions for OLE controls](../vs140/Dialog-Data-Exchange-Functions-for-OLE-Controls.md)  
  
-   [Macros and globals to aid in calling Open Database Connectivity (ODBC) API functions directly](../vs140/Database-Macros-and-Globals.md)  
  
-   [DAO database engine initialization and termination](../vs140/DAO-Database-Engine-Initialization-and-Termination.md)  
  
## Internet  
  
-   [Internet URL parsing globals](../vs140/Internet-URL-Parsing-Globals.md)  
  
## DHTML / DHTML Event Maps  
  
-   [DHTML dialog data exchange (DDX) helper macros](../vs140/DDX_DHtml-Helper-Macros.md)  
  
-   [DHTML event maps](../vs140/DHTML-Event-Maps.md)  
  
## OLE  
  
-   [OLE initialization](../vs140/OLE-Initialization.md)  
  
-   [Application control](../vs140/Application-Control.md)  
  
-   [Dispatch maps](../vs140/Dispatch-Maps.md)  
  
 In addition, MFC provides a function called [AfxEnableControlContainer](../vs140/AfxEnableControlContainer.md) that enables any OLE container developed with MFC 4.0 to fully support embedded OLE controls.  
  
## OLE Controls  
  
-   [Variant parameter type constants](../vs140/Variant-Parameter-Type-Constants.md)  
  
-   [Type library access](../vs140/Type-Library-Access.md)  
  
-   [Property pages](../vs140/Property-Pages--MFC-.md)  
  
-   [Event maps](../vs140/Event-Maps.md)  
  
-   [Event sink maps](../vs140/Event-Sink-Maps.md)  
  
-   [Connection maps](../vs140/Connection-Maps.md)  
  
-   [Registering OLE controls](../vs140/Registering-OLE-Controls.md)  
  
-   [Class factories and licensing](../vs140/Class-Factories-and-Licensing.md)  
  
-   [Persistence of OLE controls](../vs140/Persistence-of-OLE-Controls.md)  
  
 The first part of this section briefly discusses each of the previous categories and lists the globals and macros in the category, together with brief descriptions of functionality. Following this are descriptions of the global functions, global variables, and macros in the MFC library.  
  
> [!NOTE]
>  Many global functions start with the prefix "Afx", but some, for example, the dialog data exchange (DDX) functions and many of the database functions, do not follow this convention. All global variables start with "afx" as a prefix. Macros do not start with any particular prefix, but they are written in uppercase letters.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)