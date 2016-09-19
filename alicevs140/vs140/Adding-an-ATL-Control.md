---
title: "Adding an ATL Control"
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
ms.topic: reference
ms.assetid: 10223e7e-fdb7-4163-80c6-44aeafa8e6ce
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Adding an ATL Control
Use this wizard to add a user interface object to a project that supports interfaces for all potential containers. To support these interfaces, the project must have been created as an ATL application or as an MFC application that contains ATL support. You can use the [ATL Project Wizard](../vs140/ATL-Project-Wizard.md) to create an ATL application, or [add an ATL object to your MFC application](../vs140/Adding-ATL-Support-to-Your-MFC-Project.md) to implement ATL support for an MFC application.  
  
### To add an ATL control to your project  
  
1.  In either **Solution Explorer** or [Class View](assetId:///8d7430a9-3e33-454c-a9e1-a85e3d2db925), right-click the name of the project to which you want to add the ATL simple object.  
  
2.  Click **Add** from the shortcut menu, and then click **Add Class**.  
  
3.  In the [Add Class](../vs140/Add-Class-Dialog-Box.md) dialog box, in the templates pane, click **ATL Control**, and then click **Add** to display the [ATL Control Wizard](../vs140/ATL-Control-Wizard.md).  
  
 Using the **ATL Control Wizard**, you can create one of three types of controls:  
  
-   A standard control  
  
-   A composite control  
  
-   A DHTML control  
  
 Additionally, you can reduce the size of the control and remove interfaces that are not used by most containers by selecting **Minimal control** on the **Options** page of the wizard.  
  
## See Also  
 [Adding Functionality to the Composite Control](../vs140/Adding-Functionality-to-the-Composite-Control.md)   
 [Fundamentals of ATL COM Objects](../vs140/Fundamentals-of-ATL-COM-Objects.md)   
 [ATLFire Sample](assetId:///5b2649f1-f45b-4cfb-9c4b-4d9459c26b09)