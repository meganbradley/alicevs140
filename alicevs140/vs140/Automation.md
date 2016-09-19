---
title: "Automation"
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
ms.assetid: 329117f0-c1aa-4680-a901-bfb71277dfba
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Automation
Automation (formerly known as OLE Automation) makes it possible for one application to manipulate objects implemented in another application, or to expose objects so they can be manipulated.  
  
 An [Automation server](../vs140/Automation-Servers.md) is an application (a type of COM server) that exposes its functionality through COM interfaces to other applications, called [Automation clients](../vs140/Automation-Clients.md). The exposure enables Automation clients to automate certain functions by directly accessing objects and using the services they provide.  
  
 Automation servers and clients use COM interfaces that are always derived from `IDispatch` and take and return a specific set of data types called Automation types. You can automate any object that exposes an Automation interface, providing methods and properties that you can access from other applications. Automation is available for both OLE and COM objects. The automated object might be local or remote (on another machine accessible across a network); therefore there are two categories of automation:  
  
-   Automation (local).  
  
-   [Remote Automation](../vs140/Remote-Automation.md) (over a network, using Distributed COM, or DCOM).  
  
 Exposing objects is beneficial when applications provide functionality useful to other applications. For example, an ActiveX control is a type of Automation server; the application hosting the ActiveX control is the automation client of that control.  
  
 As another example, a word processor might expose its spell-checking functionality to other programs. Exposure of objects enables vendors to improve their applications by using the ready-made functionality of other applications. In this way, Automation applies some of the principles of object-oriented programming, such as reusability and encapsulation, at the level of applications themselves.  
  
 More important is the support Automation provides to users and solution providers. By exposing application functionality through a common, well-defined interface, Automation makes it possible to build comprehensive solutions in a single general programming language, such as Microsoft Visual Basic, instead of in diverse application-specific macro languages.  
  
 Many commercial applications, such as Microsoft Excel and Microsoft Visual C++, allow you to automate much of their functionality. For example, in Visual C++, you can write [VBScript](vtoriVBScript) macros to automate builds, aspects of code editing, or debugging tasks.  
  
##  <a name="_core_passing_parameters_in_automation"></a> Passing Parameters in Automation  
 One difficulty in creating Automation methods is helping to provide a uniform "safe" mechanism to pass data between automation servers and clients. Automation uses the **VARIANT** type to pass data. The **VARIANT** type is a tagged union. It has a data member for the value (this is an anonymous C++ union) and a data member indicating the type of information stored in the union. The **VARIANT** type supports a number of standard data types: 2- and 4-byte integers, 4- and 8-byte floating-point numbers, strings, and Boolean values. In addition, it supports the `HRESULT` (OLE error codes), **CURRENCY** (a fixed-point numeric type), and **DATE** (absolute date and time) types, as well as pointers to **IUnknown** and `IDispatch` interfaces.  
  
 The **VARIANT** type is encapsulated in the [COleVariant](../vs140/COleVariant-Class.md) class. The supporting **CURRENCY** and **DATE** classes are encapsulated in the [COleCurrency](../vs140/COleCurrency-Class.md) and [COleDateTime](../vs140/COleDateTime-Class.md) classes.  
  
## Automation Samples  
  
-   [AUTOCLIK](../vs140/Visual-C---Samples.md) Use this sample to learn Automation techniques and as a foundation for learning Remote Automation.  
  
-   [ACDUAL](../vs140/Visual-C---Samples.md) Adds dual interfaces to an Automation server application.  
  
-   [CALCDRIV](../vs140/Visual-C---Samples.md) Automation client application driving MFCCALC.  
  
-   [INPROC](../vs140/Visual-C---Samples.md) Demonstrates an In-Process Automation server application.  
  
-   [IPDRIVE](../vs140/Visual-C---Samples.md) Automation client application driving INPROC.  
  
-   [MFCCALC](../vs140/Visual-C---Samples.md) Demonstrates an Automation client application.  
  
## What do you want to know more about?  
  
-   [Automation Clients](../vs140/Automation-Clients.md)  
  
-   [Automation Servers](../vs140/Automation-Servers.md)  
  
-   [Remote Automation](../vs140/Remote-Automation.md)  
  
-   [OLE](../vs140/OLE-in-MFC.md)  
  
-   [Active Technology](../vs140/MFC-COM.md)  
  
## What do you want to do?  
  
-   [Add an Automation class](../vs140/Automation-Servers.md)  
  
-   [Use type libraries](../vs140/Automation-Clients--Using-Type-Libraries.md)  
  
-   [Pass parameters in Automation](#_core_automation_topics)  
  
-   [Access automation servers](../vs140/Automation-Servers.md)  
  
-   [Write automation clients in C++](../vs140/Automation-Clients.md)  
  
## See Also  
 [MFC COM](../vs140/MFC-COM.md)