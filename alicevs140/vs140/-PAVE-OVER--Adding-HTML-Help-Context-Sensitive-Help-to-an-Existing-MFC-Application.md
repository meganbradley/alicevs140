---
title: "&lt;PAVE OVER&gt; Adding HTML Help Context-Sensitive Help to an Existing MFC Application"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d9ca809e-66dc-4ad3-9796-881c2c7b91e3
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; Adding HTML Help Context-Sensitive Help to an Existing MFC Application
If an MFC application was created without the context-sensitive help wizard option, you can subsequently add context-sensitive help.  
  
### To add context-sensitive help in HTMLHelp format to an MFC application  
  
1.  Run the MFC Application Wizard and choose the context-sensitive Help option to create a new application that has the help-related files and code. We will call this project HasHelp.  
  
2.  Follow the steps in [Copying Help-Specific Resources to Your Project](../vs140/-PAVE-OVER--Copying-Help-Specific-Resources-to-Your-Project.md).  
  
3.  Follow the instructions in [Copying the Help Message Map Commands](../vs140/-PAVE-OVER--Copying-the-Help-Message-Map-Commands.md).  
  
4.  Copy the files from the hlp directory for the project that was created to use context-sensitive help in HTMLHelp format.  
  
5.  Rename the *.hh\* files so the file names match the name of the application you are developing.  
  
6.  Open the .hhp file in HTMLHelp Workshop and change the file names in the .hhp file to match the *.hh\* files in your project.  
  
7.  Place the following line in the constructor for the *AppName* module (where *AppName* is the name of the application; this example uses an application called Test):  
  
     [!CODE [NVC_MFCHtmlHelp#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCHtmlHelp#4)]  
  
8.  Examine the .vcxproj file (use Notepad) of the project that was created to use context-sensitive help in HTMLHelp format and notice the custom build steps used to create the help file (.chm file) when the project is built. Do a search for VCCustomBuildTool in the .vcxproj file to locate these custom build steps. Copy those same custom build steps into your project.  Replace all occurrences of HasHelp with the name of your project.  
  
## See Also  
 [HTML Help: Context-Sensitive Help for Your Programs](../vs140/HTML-Help--Context-Sensitive-Help-for-Your-Programs.md)