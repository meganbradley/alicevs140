---
title: "-DRIVER (Windows NT Kernel Mode Driver)"
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
H1: /DRIVER (Windows NT Kernel Mode Driver)
ms.assetid: aeee8e28-5d97-40f5-ba16-9f370fe8a1b8
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -DRIVER (Windows NT Kernel Mode Driver)
```  
/DRIVER[:UPONLY | :WDM]  
```  
  
## Remarks  
 Use the /DRIVER linker option to build a Windows NT kernel mode driver.  
  
 **/DRIVER:UPONLY** causes the linker to add the **IMAGE_FILE_UP_SYSTEM_ONLY** bit to the characteristics in the output header to specify that it is a uniprocessor (UP) driver. The operating system will refuse to load a UP driver on a multiprocessor (MP) system.  
  
 **/DRIVER:WDM** causes the linker to set the **IMAGE_DLLCHARACTERISTICS_WDM_DRIVER** bit in the optional header's DllCharacteristics field.  
  
 If **/DRIVER** is not specified, these bits are not set by the linker.  
  
 If **/DRIVER** is specified:  
  
-   /FIXED:NO is in effect ([/FIXED (Fixed Base Address)](../Topic/-FIXED%20\(Fixed%20Base%20Address\).md)).  
  
-   The extension of the output file will be .sys. Use **/OUT** to change the default filename and extension ([/OUT (Output File Name)](../vs140/-OUT--Output-File-Name-.md)).  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **System** property page.  
  
4.  Modify the **Driver** property.  
  
### To set this linker option programmatically  
  
1.  See `P:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.driver`.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)