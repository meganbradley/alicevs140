---
title: "Specifying the Pathname"
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
ms.assetid: 7a6595ce-3383-44ae-957a-466bfa29c343
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specifying the Pathname
Each output-file option accepts a *pathname* argument that can specify a location and a name for the output file. The argument can include a drive name, directory, and file name. No space is allowed between the option and the argument.  
  
 If *pathname* includes a file name without an extension, the compiler gives the output a default extension. If *pathname* includes a directory but no file name, the compiler creates a file with a default name in the specified directory. The default name is based on the base name of the source file and a default extension based on the type of the output file. If you leave off *pathname* entirely, the compiler creates a file with a default name in a default directory.  
  
 Alternatively, the *pathname* argument can be a device name (AUX, CON, PRN, or NUL) rather than a file name. Do not use a space between the option and the device name or a colon as part of the device name.  
  
|Device name|Represents|  
|-----------------|----------------|  
|AUX|Auxiliary device|  
|CON|Console|  
|PRN|Printer|  
|NUL|Null device (no file created)|  
  
## Example  
 The following command line sends a mapfile to the printer:  
  
```  
CL /FmPRN HELLO.CPP  
```  
  
## See Also  
 [Output-File (/F) Options](../vs140/Output-File---F--Options.md)   
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)