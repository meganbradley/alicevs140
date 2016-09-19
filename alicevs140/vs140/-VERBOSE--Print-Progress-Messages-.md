---
title: "-VERBOSE (Print Progress Messages)"
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
H1: /VERBOSE (Print Progress Messages)
ms.assetid: 9c347d98-4c37-4724-a39e-0983934693ab
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -VERBOSE (Print Progress Messages)
```  
/VERBOSE[:{ICF|INCR|LIB|REF|SAFESEH|UNUSEDLIBS}]  
```  
  
## Remarks  
 The linker sends information about the progress of the linking session to the **Output** window. On the command line, the information is sent to standard output and can be redirected to a file.  
  
|Option|Description|  
|------------|-----------------|  
|/VERBOSE|Displays details about the linking process.|  
|/VERBOSE:ICF|Display information about linker activity that results from the use of [/OPT:ICF](../Topic/-OPT%20\(Optimizations\).md).|  
|/VERBOSE:INCR|Displays information about the incremental link process.|  
|/VERBOSE:LIB|Displays progress messages that indicate just the libraries searched.<br /><br /> The displayed information includes the library search process and lists each library and object name (with full path), the symbol being resolved from the library, and a list of objects that reference the symbol.|  
|/VERBOSE:REF|Displays information about linker activity that results from the use of [/OPT:REF](../Topic/-OPT%20\(Optimizations\).md).|  
|/VERBOSE:SAFESEH|Displays information about modules that are not compatible with safe exception handling when [/SAFESEH](../Topic/-SAFESEH%20\(Image%20has%20Safe%20Exception%20Handlers\).md) is not specified.|  
|/VERBOSE:UNUSEDLIBS|Displays information about any library files that are unused when the image is created.|  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Expand the **Linker** folder.  
  
3.  Select the **Command Line** property page.  
  
4.  Add the option to the **Additional Options** box.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ShowProgress?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)