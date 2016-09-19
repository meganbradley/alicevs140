---
title: "-TLBOUT (Name .TLB File)"
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
H1: /TLBOUT (Name .TLB File)
ms.assetid: 0df6d078-2e48-46c9-a1a5-02674d85dce8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -TLBOUT (Name .TLB File)
```  
/TLBOUT:[path\]filename  
```  
  
## Remarks  
 where:  
  
 *path*  
 An absolute or relative path specification for where the .tlb file should be created.  
  
 *filename*  
 Specifies the name of the .tlb file created by the MIDL compiler. No file extension is assumed; specify *filename*.tlb if you want a .tlb extension.  
  
## Remarks  
 The /TLBOUT option specifies the name and extension of the .tlb file.  
  
 The MIDL compiler is called by the Visual C++ linker when linking projects that have the [module](../vs140/module--C---.md) attribute.  
  
 If /TLBOUT is not specified, the .tlb file will get its name from [/IDLOUT](../vs140/-IDLOUT--Name-MIDL-Output-Files-.md) *filename*. If /IDLOUT is not specified, the .tlb file will be called vc70.tlb.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **Embedded IDL** property page.  
  
4.  Modify the **Type Library** property.  
  
### To set this linker option programmatically  
  
1.  See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.TypeLibraryFile?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)   
 [/IGNOREIDL (Don't Process Attributes into MIDL)](../Topic/-IGNOREIDL%20\(Don't%20Process%20Attributes%20into%20MIDL\).md)   
 [/MIDL (Specify MIDL Command Line Options)](../vs140/-MIDL--Specify-MIDL-Command-Line-Options-.md)   
 [Building an Attributed Program](../vs140/Building-an-Attributed-Program.md)