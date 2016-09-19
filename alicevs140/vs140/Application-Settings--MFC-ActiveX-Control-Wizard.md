---
title: "Application Settings, MFC ActiveX Control Wizard"
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
ms.assetid: 48475194-cc63-467f-8499-f142269a4c1c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Application Settings, MFC ActiveX Control Wizard
Use this page of the MFC ActiveX Control Wizard to design and add basic features to a new MFC ActiveX project. These settings apply to the application itself and not to any specific feature or element of the control.  
  
 **Run-time license**  
 Select this option to generate a user license file to distribute with the control. The license is a text file, *projname*.lic. This file must be in the same directory as the control's DLL to allow an instance of the control to be created in a design-time environment. You usually distribute this file with your control, but your customers do not distribute it.  
  
 **Generate help files**  
 Select this option to generate stubbed help files and configure the project to include help for your control. A default project, created without this option, generates only an **About** box that is displayed when the user right clicks the control, uses F1, or clicks **Help** on the control's container.  
  
> [!NOTE]
>  How help is displayed depends on how your control interacts with its container. If you include help with your container, you must handle messages between the control and the container to display the help appropriately.  
  
 When you generate help files using the wizard, your project includes the following:  
  
-   The file .vcxproj contains code to build and configure the help file when the project is built.  
  
-   The file *projnamePropPage*.cpp file includes a [SetHelpInfo](../vs140/COlePropertyPage--SetHelpInfo.md) function in the constructor.  
  
-   The file projname.hpj, is the help project file used by the help compiler to create the ActiveX control's help file. The .hpj file is a text file containing the information about building your help file and the paths to the additional files (for example, bitmaps) the help file includes.  
  
-   The project includes the HLP directory to contain the project help bitmap files and the help topic file (*projname*.rtf). This help topic file contains the standard help topics for the common properties, events, and methods supported by many ActiveX controls. You can edit the .rtf file to add or remove specific help topics.  
  
## See Also  
 [MFC ActiveX Control Wizard](../vs140/MFC-ActiveX-Control-Wizard.md)   
 [Control Names, MFC ActiveX Control Wizard](../vs140/Control-Names--MFC-ActiveX-Control-Wizard.md)   
 [Control Settings, MFC ActiveX Control Wizard](../vs140/Control-Settings--MFC-ActiveX-Control-Wizard.md)