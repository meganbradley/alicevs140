---
title: "-DLL (Build a DLL)"
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
H1: /DLL (Build a DLL)
ms.assetid: c7685aec-31d0-490f-9503-fb5171a23609
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -DLL (Build a DLL)
```  
/DLL  
```  
  
## Remarks  
 The /DLL option builds a DLL as the main output file. A DLL usually contains exports that can be used by another program. There are three methods for specifying exports, listed in recommended order of use:  
  
1.  [__declspec(dllexport)](../vs140/dllexport--dllimport.md) in the source code  
  
2.  An [EXPORTS](../vs140/EXPORTS.md) statement in a .def file  
  
3.  An [/EXPORT](../vs140/-EXPORT--Exports-a-Function-.md) specification in a LINK command  
  
 A program can use more than one method.  
  
 Another way to build a DLL is with the **LIBRARY** module-definition statement. The /BASE and /DLL options together are equivalent to the **LIBRARY** statement.  
  
 Do not specify this option within the development environment; this option is for use only on the command line. This option is set when you create a DLL project with an Application Wizard.  
  
 Note that if you create your import library in a preliminary step, before creating your .dll, you must pass the same set of object files when building the .dll, as you passed when building the import library.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Configuration Properties** folder.  
  
3.  Click the **General** property page.  
  
4.  Modify the **Configuration Type** property.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCPropertySheet.ConfigurationType?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)