---
title: "MFC ActiveX Controls: Properties"
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
ms.assetid: b678a53c-0d9e-476f-8aa0-23b80baaba46
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC ActiveX Controls: Properties
An ActiveX control fires events to communicate with its control container. The container, in return, uses methods and properties to communicate with the control. Methods and properties are similar in use and purpose, respectively, to member functions and member variables of a C++ class. Properties are data members of the ActiveX control that are exposed to any container. Properties provide an interface for applications that contain ActiveX controls, such as Automation clients and ActiveX control containers.  
  
 Properties are also called attributes.  
  
 For more information on ActiveX control methods, see the article [MFC ActiveX Controls: Methods](../vs140/MFC-ActiveX-Controls--Methods.md).  
  
 ActiveX controls can implement both stock and custom methods and properties. Class `COleControl` provides an implementation for stock properties. (For a complete list of stock properties, see the article [MFC ActiveX Controls: Adding Stock Properties](../vs140/MFC-ActiveX-Controls--Adding-Stock-Properties.md).) Custom properties, defined by the developer, add specialized capabilities to an ActiveX control. For more information, see [MFC ActiveX Controls: Adding Custom Properties](../vs140/MFC-ActiveX-Controls--Adding-Custom-Properties.md).  
  
 Both custom and stock properties, like methods, are supported by a mechanism that consists of a dispatch map that handles properties and methods and existing member functions of the `COleControl` class. In addition, these properties can have parameters that the developer uses to pass extra information to the control.  
  
 The following articles discuss ActiveX control properties in more detail:  
  
-   [MFC ActiveX Controls: Adding Stock Properties](../vs140/MFC-ActiveX-Controls--Adding-Stock-Properties.md)  
  
-   [MFC ActiveX Controls: Adding Custom Properties](../vs140/MFC-ActiveX-Controls--Adding-Custom-Properties.md)  
  
-   [MFC ActiveX Controls: Advanced Property Implementation](../vs140/MFC-ActiveX-Controls--Advanced-Property-Implementation.md)  
  
-   [MFC ActiveX Controls: Accessing Ambient Properties](../vs140/MFC-ActiveX-Controls--Accessing-Ambient-Properties.md)  
  
## See Also  
 [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)