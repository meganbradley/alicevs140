---
title: "MFC COM"
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
ms.assetid: 7646bdcb-3a06-4ed5-9386-9b00f3979dcb
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC COM
A subset of MFC is designed to support COM, while most of the Active Template Library (ATL) is designed for COM programming. This section of topics describes MFC's support for COM.  
  
 Active technologies (such as ActiveX controls, Active document containment, OLE, and so on) use the Component Object Model (COM) to enable software components to interact with one another in a networked environment, regardless of the language with which they were created. Active technologies can be used to create applications that run on the desktop or the Internet. For more information see [Introduction to COM](../vs140/Introduction-to-COM.md) or [The Component Object Model](http://msdn.microsoft.com/library/windows/desktop/ms694363).  
  
 Active technologies include both client and server technologies, including the following:  
  
-   [Active document containment](../vs140/Active-Document-Containment.md), supported in MFC versions 4.2 and later, allows users to view [active documents](../vs140/Active-Documents.md) (such as Microsoft Excel or Word files) and activate the entire interface of the document's native application in the entire client area of an [active document container](../vs140/Active-Document-Containers.md) such as the Microsoft Office Binder or Microsoft Internet Explorer. The containers act as clients, while the documents are provided by [active document servers](../vs140/Active-Document-Servers.md). For more information on using active documents in Internet applications, see: [Active Documents on the Internet](../vs140/Active-Documents-on-the-Internet.md).  
  
-   ActiveX controls are interactive objects that can be used in containers such as a Web site. For more information on ActiveX controls, see:  
  
    -   [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)  
  
    -   [ActiveX Controls on the Internet](../vs140/ActiveX-Controls-on-the-Internet.md)  
  
    -   [Overview: Internet](../vs140/MFC-Internet-Programming-Basics.md)  
  
    -   [Upgrade an Existing ActiveX Control to be Used on the Internet](../vs140/Upgrading-an-Existing-ActiveX-Control.md)  
  
    -   [Debugging an ActiveX Control](../vs140/How-to--Debug-an-ActiveX-Control.md)  
  
-   Active scripting controls the integrated behavior of one or more ActiveX controls from a browser or server. For more information on active scripting, see [Active Technology on the Internet](../vs140/Active-Technology-on-the-Internet.md).  
  
-   [Automation](../vs140/Automation.md) (formerly known as OLE Automation) makes it possible for one application to manipulate objects implemented in another application, or to "expose" objects so they can be manipulated.  
  
     The automated object might be local or [remote](../vs140/Remote-Automation.md) (on another machine accessible across a network). Automation is available for both OLE and COM objects.  
  
-   This section also provides information on how to write COM components using MFC, for example, in [Connection Points](../vs140/Connection-Points.md).  
  
 For a discussion of what is still called OLE versus what is now called active technology, see the topics on [OLE](../vs140/OLE-in-MFC.md).  
  
 Also, see Knowledge Base article Q248019 : HOWTO: Prevent Server Busy Dialog Box From Appearing During a Lengthy COM Operation.  
  
## In This Section  
 [Active Document Containment](../vs140/Active-Document-Containment.md)  
  
 [Automation](../vs140/Automation.md)  
  
 [Remote Automation](../vs140/Remote-Automation.md)  
  
 [Connection Points](../vs140/Connection-Points.md)  
  
 [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)  
  
## See Also  
 [Concepts](../vs140/MFC-Concepts.md)