---
title: "-WINMD (Generate Windows Metadata)"
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
H1: /WINMD (Generate Windows Metadata)
ms.assetid: bcfb4901-411e-4c9e-9f78-23028b6e5fcc
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -WINMD (Generate Windows Metadata)
Enables generation of a Windows Runtime Metadata (.winmd) file.  
  
```  
/WINMD[:{NO|ONLY}]  
```  
  
## Remarks  
 /WINMD  
 The default setting for [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. The linker generates both the binary executable file and the .winmd metadata file.  
  
 /WINMD:NO  
 The linker generates only the binary executable file, but not a .winmd file.  
  
 /WINMD:ONLY  
 The linker generates only the .winmd file, but not the binary executable file.  
  
 By default, the output file name has the form `binaryname`.winmd. To specify a different file name, use the [/WINMDFILE](../vs140/-WINMDFILE--Specify-winmd-File-.md) option.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Select the **Linker** folder.  
  
3.  Select the **Windows Metadata** property page.  
  
4.  In the **Generate Windows Metadata** drop-down list box, select the option you want.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)