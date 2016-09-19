---
title: "Help Files (WinHelp)"
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
ms.assetid: 4fdcbd66-66b0-4866-894a-fd7b4c2557e4
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Help Files (WinHelp)
The following files are created when you add the WinHelp type of Help support to your application by selecting the **Context-sensitive help** check box and then selecting **WinHelp format** in the [Advanced Features](../vs140/Advanced-Features--MFC-Application-Wizard.md) page of the MFC Application Wizard.  
  
|File name|Directory location|Solution Explorer location|Description|  
|---------------|------------------------|--------------------------------|-----------------|  
|*Projname*.hpj|*Projname*\hlp|Source Files|The Help project file used by the Help compiler to create your program or control's Help file.|  
|*Projname*.rtf|*Projname*\hlp|Help Files|Contains template topics that you can edit and information on customizing your .hpj file.|  
|*Projname*.cnt|*Projname*\hlp|Help Files|Provides the structure for the **Contents** window in Windows Help.|  
|Makehelp.bat|*Projname*|Source Files|Used by the system to build the Help project when the project is compiled.|  
|Print.rtf|*Projname*\hlp|Help Files|Created if your project includes printing support (the default). Describes the printing commands and dialog boxes.|  
|*.bmp|*Projname*\hlp|Resource Files|Contain images for the different generated help file topics.|  
  
 You can add WinHelp support to an MFC ActiveX Control project by selecting **Generate help files** in the [Application Settings](../vs140/Application-Settings--MFC-ActiveX-Control-Wizard.md) tab of the MFC ActiveX Control Wizard. The following files are added to your project when you add Help support to an MFC ActiveX control:  
  
|File name|Directory location|Solution Explorer location|Description|  
|---------------|------------------------|--------------------------------|-----------------|  
|*Projname*.hpj|*Projname*\hlp|Source files|The project file used by the Help compiler to create your program or control's Help file.|  
|*Projname*.rtf|*Projname*\hlp|Project|Contains template topics that you can edit and information on customizing your .hpj file.|  
|Makehelp.bat|*Projname*|Source Files|Used by the system to build the Help project when the project is compiled.|  
|Bullet.bmp|*Projname*|Resource Files|Used by standard Help file topics to represent bulleted lists.|  
  
## See Also  
 [File Types Created for Visual C++ Projects](../vs140/File-Types-Created-for-Visual-C---Projects.md)