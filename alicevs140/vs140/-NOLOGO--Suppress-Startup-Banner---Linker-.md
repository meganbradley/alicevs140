---
title: "-NOLOGO (Suppress Startup Banner) (Linker)"
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
H1: /NOLOGO (Suppress Startup Banner) (Linker)
ms.assetid: 3b20dddd-eca6-4545-a331-9f70bf720197
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -NOLOGO (Suppress Startup Banner) (Linker)
```  
/NOLOGO  
```  
  
## Remarks  
 The /NOLOGO option prevents display of the copyright message and version number.  
  
 This option also suppresses echoing of command files. For details, see [LINK Command Files](../vs140/LINK-Command-Files.md).  
  
 By default, this information is sent by the linker to the Output window. On the command line, it is sent to standard output and can be redirected to a file.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  This option should only be used from the command line.  
  
### To set this linker option programmatically  
  
1.  This linker option cannot be changed programmatically.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)