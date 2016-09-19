---
title: "-PGD (Specify Database for Profile-Guided Optimizations)"
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
H1: /PGD (Specify Database for Profile-Guided Optimizations)
ms.assetid: 9f312498-493b-461f-886f-92652257e443
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -PGD (Specify Database for Profile-Guided Optimizations)
/PGD:`filename`  
  
## Remarks  
 where:  
  
 `filename`  
 Specifies the name of the .pgd file that will be used to hold information about the running program.  
  
## Remarks  
 When using [/LTCG:PGINSTRUMENT](../vs140/-LTCG--Link-time-Code-Generation-.md), use /PGD to specify a nondefault name or location for the .pgd file. If you do not specify /PGD, the .pgd file name will be the same as the output file (.exe or .dll) name and will be created in the same directory from which the link was invoked.  
  
 When using /LTCG:PGOPTIMIZE, use /PGD to specify the name of the .pgd file to use to create the optimized image.  
  
 For more information, see [Profile Guided Optimization](../vs140/Profile-Guided-Optimizations.md).  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Expand the **Configuration Properties** node.  
  
3.  Expand the **Linker** node.  
  
4.  Select the **Optimization** property page.  
  
5.  Modify the **Profile Guided Database** property.  
  
### To set this linker option programmatically  
  
1.  See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ProfileGuidedDatabase?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)