---
title: "-HEAP (Set Heap Size)"
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
H1: /HEAP (Set Heap Size)
ms.assetid: a3f71927-7f1d-492c-9fdb-dfccb1a043da
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -HEAP (Set Heap Size)
```  
/HEAP:reserve[,commit]  
```  
  
## Remarks  
 The /HEAP option sets the size of the heap in bytes. This option is only for use when building an .exe file.  
  
 The *reserve* argument specifies the total heap allocation in virtual memory. The default heap size is 1 MB. The linker rounds up the specified value to the nearest 4 bytes.  
  
 The optional `commit` argument is subject to interpretation by the operating system. In Windows NT/Windows 2000, it specifies the amount of physical memory to allocate at a time. Committed virtual memory causes space to be reserved in the paging file. A higher `commit` value saves time when the application needs more heap space, but increases the memory requirements and possibly the startup time.  
  
 Specify the *reserve* and `commit` values in decimal or C-language notation.  
  
 This functionality is also available via a module definition file with [HEAPSIZE](../vs140/HEAPSIZE.md).  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **System** property page.  
  
4.  Modify the **Heap Commit Size** property.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.HeapReserveSize?qualifyHint=False> and <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.HeapCommitSize?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)