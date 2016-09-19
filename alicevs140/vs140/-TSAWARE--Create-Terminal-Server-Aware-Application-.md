---
title: "-TSAWARE (Create Terminal Server Aware Application)"
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
H1: /TSAWARE (Create Terminal Server Aware Application)
ms.assetid: fe1c1846-de5b-4839-b562-93fbfe36cd29
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -TSAWARE (Create Terminal Server Aware Application)
```  
/TSAWARE[:NO]  
```  
  
## Remarks  
 The /TSAWARE option sets a flag in the IMAGE_OPTIONAL_HEADER DllCharacteristics field in the program image's optional header. When this flag is set, Terminal Server will not make certain changes to the application.  
  
 When an application is not Terminal Server aware (also known as a legacy application), Terminal Server makes certain modifications to the legacy application to make it work properly in a multiuser environment. For example, Terminal Server will create a virtual Windows folder, such that each user gets a Windows folder instead of getting the system's Windows directory. This gives users access to their own INI files. In addition, Terminal Server makes some adjustments to the registry for a legacy application. These modifications slow the loading of the legacy application on Terminal Server.  
  
 If an application is Terminal Server aware, it must neither rely on INI files nor write to the **HKEY_CURRENT_USER** registry during setup.  
  
 If you use /TSAWARE and your application still uses INI files, the files will be shared by all users of the system. If that is acceptable, you can still link your application with /TSAWARE; otherwise you need to use /TSAWARE:NO.  
  
 The /TSAWARE option is enabled by default for Windows 2000 and later, for Windows and console applications. See [/SUBSYSTEM](../Topic/-SUBSYSTEM%20\(Specify%20Subsystem\).md) and [/VERSION](../Topic/-VERSION%20\(Version%20Information\).md) for information.  
  
 /TSAWARE is not valid for drivers, VxDs, or DLLs.  
  
 If an application was linked with /TSAWARE, DUMPBIN [/HEADERS](../vs140/-HEADERS.md) will display information to that effect.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **System** property page.  
  
4.  Modify the **Terminal Server** property.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.TerminalServerAware?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)   
 [Storing User-Specific Information](http://msdn.microsoft.com/library/aa383452)   
 [Legacy Applications in a Terminal Services Environment](https://msdn.microsoft.com/en-us/library/aa382957.aspx)