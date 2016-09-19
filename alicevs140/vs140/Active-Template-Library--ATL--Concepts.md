---
title: "Active Template Library (ATL) Concepts"
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
ms.assetid: a3960991-4d76-4da5-9568-3fa7fde53ff4
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Active Template Library (ATL) Concepts
The Active Template Library (ATL) is a set of template-based C++ classes that let you create small, fast Component Object Model (COM) objects. It has special support for key COM features, including stock implementations, dual interfaces, standard COM enumerator interfaces, connection points, tear-off interfaces, and ActiveX controls.  
  
 If you do a lot of ATL programming, you will want to learn more about attributes, a new feature in Visual C++ .NET that is designed to simplify COM programming. For more information, see [Attributed Programming](../vs140/Attributed-Programming-Concepts.md).  
  
## In This Section  
 [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md)  
 Leads you through the creation of a control and demonstrates some ATL fundamentals in the process.  
  
 [Introduction to COM and ATL](../vs140/Introduction-to-COM-and-ATL.md)  
 Introduces the major concepts behind the Component Object Model (COM). This article also briefly explains what ATL is and when you should use it.  
  
 [Fundamentals of ATL COM Objects](../vs140/Fundamentals-of-ATL-COM-Objects.md)  
 Discusses the relationship among various ATL classes and how those classes are implemented.  
  
 [Dual Interfaces and ATL](../vs140/Dual-Interfaces-and-ATL.md)  
 Describes dual interfaces from an ATL perspective.  
  
 [ATL Collections and Enumerators](../vs140/ATL-Collections-and-Enumerators.md)  
 Describes the implementation and creation of collections and enumerators in ATL.  
  
 [Composite Control Fundamentals](../vs140/ATL-Composite-Control-Fundamentals.md)  
 Provides step-by-step instructions for creating a composite control. A composite control is a type of ActiveX control that can contain other ActiveX controls or Windows controls.  
  
 [ATL Control Containment FAQ](../vs140/ATL-Control-Containment-FAQ.md)  
 Covers the fundamental questions related to hosting controls with ATL.  
  
 [ATL COM Property Pages](../vs140/ATL-COM-Property-Pages.md)  
 Shows you how to specify and implement COM property pages.  
  
 [ATL Support for DHTML Controls](../vs140/ATL-Support-for-DHTML-Controls.md)  
 Provides step-by-step instructions for creating a DHTML control.  
  
 [ATL Connection Points](../vs140/ATL-Connection-Points.md)  
 Explains what connection points are and how ATL implements them.  
  
 [Event Handling and ATL](../vs140/Event-Handling-and-ATL.md)  
 Describes the steps that you need to take to handle COM events using ATL's [IDispEventImpl](../vs140/IDispEventImpl-Class.md) and [IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md) classes.  
  
 [ATL and the Free Threaded Marshaler](../vs140/ATL-and-the-Free-Threaded-Marshaler.md)  
 Provides details on the ATL Simple Object Wizard's option that allows your class to aggregate the free threaded marshaler (FTM).  
  
 [Specifying the Project's Threading Model](../vs140/Specifying-the-Threading-Model-for-a-Project--ATL-.md)  
 Describes the macros that are available to control run-time performance related to threading in your project.  
  
 [ATL Module Classes](../vs140/ATL-Module-Classes.md)  
 Discusses the module classes new for ATL 7.0. Module classes implement the basic functionality required by ATL.  
  
 [ATL Services](../vs140/ATL-Services.md)  
 Covers the series of events that occur when a service is implemented. Also talks about some of the concepts related to developing a service.  
  
 [ATL Window Classes](../vs140/ATL-Window-Classes.md)  
 Describes how to create, superclass, and subclass windows in ATL. The ATL window classes are not COM classes.  
  
 [ATL Collection Classes](../vs140/ATL-Collection-Classes.md)  
 Describes how to use arrays and maps in ATL.  
  
 [The ATL Registry Component (Registrar)](../vs140/ATL-Registry-Component--Registrar-.md)  
 Discusses ATL scripting syntax and replaceable parameters. It also explains how to set up a static link to the Registrar.  
  
 [Programming with ATL and C Run-Time Code](../vs140/Programming-with-ATL-and-C-Run-Time-Code.md)  
 Discusses the benefits of linking statically or dynamically to the C Run-Time Library (CRT).  
  
 [Programming with CComBSTR](../vs140/Programming-with-CComBSTR--ATL-.md)  
 Discusses several situations that require caution when programming with `CComBSTR`.  
  
 [ATL Encoding Reference](../vs140/ATL-Encoding-Reference.md)  
 Provides functions and macros that support encoding in a range of common Internet standards such as uuencode, hexadecimal, and UTF8 in atlenc.h.  
  
 [ATL Utilities Reference](../vs140/ATL-Utilities-Reference.md)  
 Provides code for manipulating paths and URLs in the form of [CPathT](../vs140/CPathT-Class.md) and [CUrl](../vs140/CUrl-Class.md). A thread pool, [CThreadPool](../vs140/CThreadPool-Class.md), can be used in your own applications. This code can be found in atlpath.h and atlutil.h.  
  
## Related Sections  
 [ATL Samples](../vs140/Visual-C---Samples.md)  
 Provides descriptions of and links to the ATL sample programs.  
  
 [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md)  
 Contains information on the ATL Project Wizard.  
  
 [ATL Control Wizard](../vs140/ATL-Control-Wizard.md)  
 Discusses how to add classes.  
  
 [Attributed Programming](../vs140/Attributed-Programming-Concepts.md)  
 Provides an overview on using attributes to simplify COM programming plus a list of links to more detailed topics.  
  
 [ATL Class Overview](../vs140/ATL-Class-Overview.md)  
 Provides reference information and links to the ATL classes.