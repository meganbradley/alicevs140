---
title: "Creating an MFC ActiveX Control Container"
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
ms.assetid: ec70e137-7c14-4940-bd0e-fd4edcc63ea5
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating an MFC ActiveX Control Container
An ActiveX control container is a parent program that supplies the environment for an ActiveX (formerly OLE) control to run. You can create an application capable of containing ActiveX controls with or without MFC, but it is much easier to do with MFC.  
  
 Creating an MFC container program using the [MFC Application Wizard](../vs140/MFC-Application-Wizard.md) allows you to access the many features of ActiveX controls and Automation that are implemented by the MFC and ActiveX classes. These features include visual editing, Automation, creating compound files, and support for controls. The MFC Application Wizard visual editing options that your parent program will support include creating a container, a mini-server, a full-server, and a program that is both a container and a server.  
  
-   **New MFC Application**. To create a new MFC program that includes Automation, visual editing, compound files, or control support, use the MFC Application Wizard and choose the appropriate Automation options.  
  
-   **Existing MFC Application**. If you are adding control containment to an existing MFC application, see [OLE Control Containers: Manually Enabling OLE Control Containment](../vs140/ActiveX-Control-Containers--Manually-Enabling-ActiveX-Control-Containment.md).  
  
### To create an ActiveX container for any of the following types of applications  
  
1.  [Containers](../vs140/Containers.md)  
  
2.  [Visual editing](../vs140/OLE--MFC-.md)  
  
3.  [MFC ActiveX controls](../vs140/MFC-ActiveX-Controls.md)  
  
## See Also  
 [Visual C++ Project Types](../vs140/Visual-C---Project-Types.md)