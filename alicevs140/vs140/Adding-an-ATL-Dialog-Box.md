---
title: "Adding an ATL Dialog Box"
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
ms.assetid: 152a378f-7b24-4f66-aeba-c740973f03a6
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Adding an ATL Dialog Box
To add an ATL dialog to your project, your project must be either an ATL project or an MFC project that includes ATL support. You can use the [ATL Project Wizard](../vs140/ATL-Project-Wizard.md) to create an ATL application, or [add an ATL object to your MFC application](../vs140/Adding-ATL-Support-to-Your-MFC-Project.md) to implement ATL support for an MFC application.  
  
 By default, the ATL Dialog Wizard implements a dialog box derived from [CAxDialogImpl](../vs140/CAxDialogImpl-Class.md). This class includes support for hosting ActiveX and Windows controls. If you do not want the overhead of ActiveX control support, once the wizard has generated your code, replace all instances of `CAxDialogImpl` with either [CSimpleDialog](../vs140/CSimpleDialog-Class.md) or [CDialogImpl](../vs140/CDialogImpl-Class.md) as your base class.  
  
> [!NOTE]
>  `CSimpleDialog` creates only modal dialog boxes that support only Windows common controls. `CDialogImpl` creates either modal or modeless dialog boxes.  
  
### To add an ATL dialog resource to your project  
  
1.  Create an ATL project using the [ATL Project Wizard](../vs140/ATL-Project-Wizard.md).  
  
2.  From [Class View](assetId:///8d7430a9-3e33-454c-a9e1-a85e3d2db925), right-click the project name and click **Add** from the shortcut menu. Click **Add Class**.  
  
3.  In the Templates pane of the [Add Class](../vs140/Add-Class-Dialog-Box.md) dialog box, click **ATL Dialog**. Click **Open** to display the [ATL Dialog Wizard](../vs140/ATL-Dialog-Wizard.md).  
  
 For more information, see [Implementing a Dialog Box](../vs140/Implementing-a-Dialog-Box.md).  
  
## See Also  
 [Adding a Class](../vs140/Adding-a-Class--Visual-C---.md)   
 [Window Classes](../vs140/ATL-Window-Classes.md)   
 [Message Maps](../vs140/Message-Maps--ATL-.md)