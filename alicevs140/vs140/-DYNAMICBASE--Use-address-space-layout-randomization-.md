---
title: "-DYNAMICBASE (Use address space layout randomization)"
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
H1: /DYNAMICBASE (Use address space layout randomization)
ms.assetid: 6c0ced8e-fe9c-4b63-b956-eb8a55fbceb2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -DYNAMICBASE (Use address space layout randomization)
Specifies whether to generate an executable image that can be randomly rebased at load time by using the address space layout randomization (ASLR) feature of [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)].  
  
## Syntax  
  
```  
/DYNAMICBASE[:NO]  
```  
  
## Remarks  
 By default, /DYNAMICBASE is on.  
  
 This option modifies the header of an executable to indicate whether the application should be randomly rebased at load time.  
  
 Address space layout randomization is supported on [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)].  
  
### To set this linker option in Visual Studio  
  
1.  Open the project **Property Pages** dialog box. For more information, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Expand the **Configuration Properties** node.  
  
3.  Expand the **Linker** node.  
  
4.  Select the **Advanced** property page.  
  
5.  Modify the **Randomized Base Address** property.  
  
### To set this linker option programmatically  
  
1.  See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.RandomizedBaseAddress?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)