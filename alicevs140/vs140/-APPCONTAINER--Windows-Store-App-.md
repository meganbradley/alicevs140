---
title: "-APPCONTAINER (Windows Store App)"
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
H1: /APPCONTAINER (Windows Store App)
ms.assetid: 9a432db5-7640-460b-ab18-6f61fa7daf6f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -APPCONTAINER (Windows Store App)
Specifies whether the linker creates an executable image that must be run in an app container.  
  
## Syntax  
  
```  
/APPCONTAINER[:NO]  
```  
  
## Remarks  
 By default, /APPCONTAINER is off.  
  
 This option modifies an executable to indicate whether the app must be run in the appcontainer process-isolation environment. Specify /APPCONTAINER for an app that must run in the appcontainer environment—for example, a [!INCLUDE[win8_appstore_long](../vs140/includes/win8_appstore_long_md.md)] app. (The option is set automatically in Visual Studio when you create a [!INCLUDE[win8_appstore_long](../vs140/includes/win8_appstore_long_md.md)] app from a template.) For a desktop app, specify /APPCONTAINER:NO or just omit the option.  
  
 The /APPCONTAINER option was introduced in [!INCLUDE[win8](../vs140/includes/win8_md.md)].  
  
### To set this linker option in Visual Studio  
  
1.  Open the project **Property Pages** dialog box. For more information, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Expand the **Configuration Properties** node.  
  
3.  Expand the **Linker** node.  
  
4.  Select the **Command Line** property page.  
  
5.  In **Additional Options**, enter `/APPCONTAINER` or `/APPCONTAINER:NO`.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)