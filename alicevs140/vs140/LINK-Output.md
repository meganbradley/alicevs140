---
title: "LINK Output"
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
ms.assetid: a98b557c-1947-447a-be1f-616fb45a9580
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LINK Output
Link output includes .exe files, DLLs, mapfiles, and messages.  
  
##  <a name="_core_output_files"></a> Output Files  
 The default output file from LINK is an .exe file. If the [/DLL](../vs140/-DLL--Build-a-DLL-.md) option is specified, LINK builds a .dll file. You can control the output file name with the [Output File Name (/OUT)](../vs140/-OUT--Output-File-Name-.md) option.  
  
 In incremental mode, LINK creates an .ilk file to hold status information for later incremental builds of the program. For details about .ilk files, see [.ilk Files](../vs140/.Ilk-Files-as-Linker-Input.md). For more information about incremental linking, see the [Link Incrementally (/INCREMENTAL)](../Topic/-INCREMENTAL%20\(Link%20Incrementally\).md) option.  
  
 When LINK creates a program that contains exports (usually a DLL), it also builds a .lib file, unless an .exp file was used in the build. You can control the import library file name with the [/IMPLIB](../vs140/-IMPLIB--Name-Import-Library-.md) option.  
  
 If the [Generate Mapfile (/MAP)](../vs140/-MAP--Generate-Mapfile-.md) option is specified, LINK creates a mapfile.  
  
 If the [Generate Debug Info (/DEBUG)](../Topic/-DEBUG%20\(Generate%20Debug%20Info\).md) option is specified, LINK creates a PDB to contain debugging information for the program.  
  
##  <a name="_core_other_output"></a> Other Output  
 When you type `link` without any other command-line input, LINK displays a usage statement that summarizes its options.  
  
 LINK displays a copyright and version message and echoes command-file input, unless the [Suppress Startup Banner (/NOLOGO)](../vs140/-NOLOGO--Suppress-Startup-Banner---Linker-.md) option is used.  
  
 You can use the [Print Progress Messages (/VERBOSE)](../vs140/-VERBOSE--Print-Progress-Messages-.md) option to display additional details about the build.  
  
 LINK issues error and warning messages in the form LNK*nnnn*. This error prefix and range of numbers are also used by LIB, DUMPBIN, and EDITBIN.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)