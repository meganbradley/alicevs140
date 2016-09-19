---
title: "Dialog Boxes"
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
ms.assetid: e4feea1a-8360-4ccb-9b84-507f1ccd9ef3
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Dialog Boxes
Applications for Windows frequently communicate with the user through dialog boxes. Class [CDialog](../vs140/CDialog-Class.md) provides an interface for managing dialog boxes, the Visual C++ dialog editor makes it easy to design dialog boxes and create their dialog-template resources, and Code wizards simplify the process of initializing and validating the controls in a dialog box and of gathering the values entered by the user.  
  
 Dialog boxes contain controls, including:  
  
-   Windows common controls such as edit boxes, pushbuttons, list boxes, combo boxes, tree controls, list controls, and progress indicators.  
  
-   ActiveX controls.  
  
-   Owner-drawn controls: controls that you are responsible for drawing in the dialog box.  
  
 Most dialog boxes are modal, which require the user to close the dialog box before using any other part of the program. But it is possible to create modeless dialog boxes, which let users work with other windows while the dialog box is open. MFC supports both kinds of dialog box with class `CDialog`. The controls are arranged and managed using a dialog-template resource, created with the [dialog editor](../vs140/Dialog-Editor.md).  
  
 [Property sheets](../vs140/Property-Sheets--MFC-.md), also known as tab dialog boxes, are dialog boxes that contain "pages" of distinct dialog-box controls. Each page has a file folder "tab" at the top. Clicking a tab brings that page to the front of the dialog box.  
  
## What do you want to know more about?  
  
-   [Example: Displaying a Dialog Box via a Menu Command](../vs140/Example--Displaying-a-Dialog-Box-via-a-Menu-Command.md)  
  
-   [Dialog-box components in the framework](../vs140/Dialog-Box-Components-in-the-Framework.md)  
  
-   [Modal and modeless dialog boxes](../vs140/Modal-and-Modeless-Dialog-Boxes.md)  
  
-   [Property sheets and property pages](../vs140/Property-Sheets-and-Property-Pages--MFC-.md) in a dialog box  
  
-   [Creating the dialog resource](../vs140/Creating-the-Dialog-Resource.md)  
  
-   [Creating a dialog class with Code Wizards](../vs140/Creating-a-Dialog-Class-with-Code-Wizards.md)  
  
-   [Life cycle of a dialog box](../vs140/Life-Cycle-of-a-Dialog-Box.md)  
  
-   [Dialog data exchange (DDX) and validation (DDV)](../vs140/Dialog-Data-Exchange-and-Validation.md)  
  
-   [Type-safe access to controls in a dialog box](../vs140/Type-Safe-Access-to-Controls-in-a-Dialog-Box.md)  
  
-   [Mapping Windows messages to your class](../vs140/Mapping-Windows-Messages-to-Your-Class.md)  
  
-   [Commonly Overridden Member Functions](../vs140/Commonly-Overridden-Member-Functions.md)  
  
-   [Commonly Added Member Functions](../vs140/Commonly-Added-Member-Functions.md)  
  
-   [Common dialog classes](../vs140/Common-Dialog-Classes.md)  
  
-   [Dialog boxes in OLE](../vs140/Dialog-Boxes-in-OLE.md)  
  
-   Create an application whose user interface is a dialog box: see the [CMNCTRL1](../vs140/Visual-C---Samples.md) or [CMNCTRL2](../vs140/Visual-C---Samples.md) sample programs. The Application Wizard provides this option as well.  
  
-   [Samples](../vs140/Dialog-Sample-List.md)  
  
## See Also  
 [User Interface Elements](../vs140/User-Interface-Elements--MFC-.md)