---
title: "General, Manifest Tool, Configuration Properties, &lt;Projectname&gt; Property Pages Dialog Box"
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
ms.assetid: b99368a5-6819-482c-a06e-f2409290cfd1
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# General, Manifest Tool, Configuration Properties, &lt;Projectname&gt; Property Pages Dialog Box
Use this dialog box to specify general options for [Mt.exe](http://msdn.microsoft.com/library/aa375649).  
  
 To access this property page dialog box, open the property pages for your project or your property sheet. Expand the **Manifest Tool** node under **Configuration Properties**, and then select **General**.  
  
## UIElement List  
 **Suppress Startup Banner**  
 **Yes (/nologo)** specifies that standard Microsoft copyright data will be concealed when the manifest tool is started. Use this option to suppress unwanted output in log files, when you run mt.exe as part of a build process or from a build environment.  
  
 **Verbose Output**  
 **Yes (/verbose)** specifies that additional build information will be displayed during manifest generation.  
  
 **Assembly Identity**  
 Uses the /identity option to specify an identity string, which comprises the attributes for the [<assemblyIdentity\> Element (ClickOnce Reference)](../vs140/-assemblyIdentity--Element--ClickOnce-Application-.md). An identity string begins with the value for the `name` attribute, and is followed by *attribute* = *value* pairs. The attributes in an identity string are delimited by a comma.  
  
 The following is an example identity string:  
  
 `Microsoft.Windows.Common-Controls, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=6595b64144ccf1df`  
  
## See Also  
 [ClickOnce Application Manifest](../vs140/ClickOnce-Application-Manifest.md)   
 [Manifest Tool Property Pages](../vs140/Manifest-Tool-Property-Pages.md)   
 [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md)   
 [How to: Edit Project Property Sheets](../vs140/How-to--Edit-Project-Property-Sheets.md)