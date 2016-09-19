---
title: "-IMPLIB (Name Import Library)"
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
H1: /IMPLIB (Name Import Library)
ms.assetid: fe8f71ab-7055-41b5-8ef8-2b97cfa4a432
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -IMPLIB (Name Import Library)
```  
/IMPLIB:filename  
```  
  
## Remarks  
 where:  
  
 *filename*  
 A user-specified name for the import library. It replaces the default name.  
  
## Remarks  
 The /IMPLIB option overrides the default name for the import library that LINK creates when it builds a program that contains exports. The default name is formed from the base name of the main output file and the extension .lib. A program contains exports if one or more of the following are specified:  
  
-   The [__declspec(dllexport)](../vs140/dllexport--dllimport.md) keyword in the source code  
  
-   [EXPORTS](../vs140/EXPORTS.md) statement in a .def file  
  
-   An [/EXPORT](../vs140/-EXPORT--Exports-a-Function-.md) specification in a LINK command  
  
 LINK ignores /IMPLIB when an import library is not being created. If no exports are specified, LINK does not create an import library. If an export file is used in the build, LINK assumes that an import library already exists and does not create one. For information on import libraries and export files, see [LIB Reference](../vs140/LIB-Reference.md).  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **Advanced** property page.  
  
4.  Modify the **Import Library** property.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ImportLibrary?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)