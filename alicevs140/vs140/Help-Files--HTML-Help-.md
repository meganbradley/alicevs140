---
title: "Help Files (HTML Help)"
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
ms.assetid: d30a1b1b-318f-4a78-8b60-93da53a224a8
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Help Files (HTML Help)
The following files are created when you add the HTML Help type of Help support to your application by selecting the **Context-sensitive help** check box and then selecting **HTML Help format** in the [Advanced Features](../vs140/Advanced-Features--MFC-Application-Wizard.md) page of the MFC Application Wizard.  
  
|File name|Directory location|Solution Explorer location|Description|  
|---------------|------------------------|--------------------------------|-----------------|  
|*Projname*.hhp|*Projname*\hlp|HTML Help files|The help project file. It contains the data needed to compile the help files into an .hxs file or a .chm file.|  
|*Projname*.hhk|*Projname*\hlp|HTML Help files|Contains an index of the help topics.|  
|*Projname*.hhc|*Projname*\hlp|HTML Help files|The contents of the help project.|  
|Makehtmlhelp.bat|*Projname*|Source Files|Used by the system to build the Help project when the project is compiled.|  
|Afxcore.htm|*Projname*\hlp|HTML Help Topics|Contains the standard help topics for standard MFC commands and screen objects. Add your own help topics to this file.|  
|Afxprint.htm|*Projname*\hlp|HTML Help Topics|Contains the help topics for the printing commands.|  
|*.jpg; \*.gif|*Projname*\hlp\Images|Resource Files|Contain images for the different generated help file topics.|  
  
## See Also  
 [File Types Created for Visual C++ Projects](../vs140/File-Types-Created-for-Visual-C---Projects.md)