---
title: "Distributing Isolated Shell Applications"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c503a985-d67a-4ef8-9123-7744a78f2f17
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Distributing Isolated Shell Applications
You must install Visual Studio and the Visual Studio SDK in order to create an isolated shell application. To distribute the application to the machines of other users or customers, you must include a special redistributable package for the isolated shell.  
  
## Prerequisites for Distributing Isolated Shell Applications  
  
|Name|Description|  
|----------|-----------------|  
|Visual Studio SDK|The SDK you must have to develop and test extensions of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. You can also use the SDK to create your own instance of the Visual Studio isolated shell.<br /><br /> Visual Studio is a prerequisite for the SDK.|  
|Microsoft Visual Studio Isolated Shell Redistributable|The redistributable that you include in your Setup program when you build a tools environment on the Visual Studio isolated shell. The isolated Shell redistributable package includes the .NET Framework 4.5.|  
  
## Creating an Installation Program for the Application  
 You must create a special installation program for your integrated or isolated shell application. For more information, see [Installing an Isolated Shell Application](../vs140/Installing-an-Isolated-Shell-Application.md).  
  
## Allowing for Updates to your Application  
 Your installation program must allow for the possibility that your application will be updated, either by Microsoft updates or by your company's updates. For more information about updates, see [Servicing Guidelines for Isolated Shell Applications](../vs140/Servicing-Guidelines-for-Isolated-Shell-Applications.md).