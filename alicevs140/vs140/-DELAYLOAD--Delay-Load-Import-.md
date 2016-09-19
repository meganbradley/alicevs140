---
title: "-DELAYLOAD (Delay Load Import)"
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
H1: /DELAYLOAD (Delay Load Import)
ms.assetid: 39ea0f1e-5c01-450f-9c75-2d9761ff9b28
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -DELAYLOAD (Delay Load Import)
```  
/DELAYLOAD:dllname  
```  
  
## Parameters  
 `dllname`  
 The name of a DLL that you want to delay load.  
  
## Remarks  
 The /DELAYLOAD option causes the DLL that's specified by `dllname` to be loaded only on the first call by the program to a function in that DLL. For more information, see [Linker Support for Delay-Loaded DLLs](../vs140/Linker-Support-for-Delay-Loaded-DLLs.md). You can use this option as many times as necessary to specify as many DLLs as you choose. You must use Delayimp.lib when you link your program, or you can implement your own delay-load helper function.  
  
 The [/DELAY](../vs140/-DELAY--Delay-Load-Import-Settings-.md) option specifies binding and loading options for each delay-loaded DLL.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  In the **Linker** folder, select the **Input** property page.  
  
3.  Modify the **Delay Loaded DLLs** property.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.DelayLoadDLLs?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)