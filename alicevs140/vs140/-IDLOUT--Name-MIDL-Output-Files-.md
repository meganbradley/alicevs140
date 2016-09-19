---
title: "-IDLOUT (Name MIDL Output Files)"
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
H1: /IDLOUT (Name MIDL Output Files)
ms.assetid: 10d00a6a-85b4-4de1-8732-e422c6931509
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -IDLOUT (Name MIDL Output Files)
```  
/IDLOUT:[path\]filename  
```  
  
## Parameters  
 *path*  
 An absolute or relative path specification. By specifying a path, you affect only the location of an .idl file; all other files are placed in the project directory.  
  
 *filename*  
 Specifies the name of the .idl file created by the MIDL compiler. No file extension is assumed; specify *filename*.idl if you want an .idl extension.  
  
## Remarks  
 The /IDLOUT option specifies the name and extension of the .idl file.  
  
 The MIDL compiler is called by the Visual C++ linker when linking projects that have the [module](../vs140/module--C---.md) attribute.  
  
 /IDLOUT also specifies the file names of the other output files associated with the MIDL compiler:  
  
-   *filename*.tlb  
  
-   *filename*_p.c  
  
-   *filename*_i.c  
  
-   *filename*.h  
  
 *filename* is the parameter that you pass to /IDLOUT. If [/TLBOUT](../vs140/-TLBOUT--Name-.TLB-File-.md) is specified, the .tlb file will get its name from /TLBOUT *filename*.  
  
 If you specify neither /IDLOUT nor /TLBOUT, the linker will create vc70.tlb, vc70.idl, vc70_p.c, vc70_i.c, and vc70.h.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **Embedded IDL** property page.  
  
4.  Modify the **Merge IDL Base File Name** property.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.MergedIDLBaseFileName?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)   
 [/IGNOREIDL (Don't Process Attributes into MIDL)](../Topic/-IGNOREIDL%20\(Don't%20Process%20Attributes%20into%20MIDL\).md)   
 [/MIDL (Specify MIDL Command Line Options)](../vs140/-MIDL--Specify-MIDL-Command-Line-Options-.md)   
 [Building an Attributed Program](../vs140/Building-an-Attributed-Program.md)