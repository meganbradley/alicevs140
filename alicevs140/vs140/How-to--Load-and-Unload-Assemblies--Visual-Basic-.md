---
title: "How to: Load and Unload Assemblies (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bbc84236-04b6-4c1b-9672-52773f65a5dc
caps.latest.revision: 5
---
# How to: Load and Unload Assemblies (Visual Basic)
The assemblies referenced by your program will automatically be loaded at build time, but it is also possible to load specific assemblies into the current application domain at runtime. For more information, see [How to: Load Assemblies into an Application Domain](assetId:///1432aa2d-bd83-4346-bf3b-a1b7920e2aa9).  
  
 There is no way to unload an individual assembly without unloading all of the application domains that contain it. Even if the assembly goes out of scope, the actual assembly file will remain loaded until all application domains that contain it are unloaded.  
  
 If you want to unload some assemblies but not others, consider creating a new application domain, executing the code inside that domain, and then unloading that application domain. For more information, see [How to: Unload an Application Domain](assetId:///f356116d-e415-4f7c-a332-6e6a60227192).  
  
### To load an assembly into an application domain  
  
1.  Use one of the several load methods contained in the classes <xref:System.AppDomain?qualifyHint=False> and <xref:System.Reflection?qualifyHint=False>. For more information, see [How to: Load Assemblies into an Application Domain](assetId:///1432aa2d-bd83-4346-bf3b-a1b7920e2aa9).  
  
### To unload an application domain  
  
1.  There is no way to unload an individual assembly without unloading all of the application domains that contain it. Use the `Unload` method from <xref:System.AppDomain?qualifyHint=False> to unload the application domains. For more information, see [How to: Unload an Application Domain](assetId:///f356116d-e415-4f7c-a332-6e6a60227192).  
  
## See Also  
 [Visual Basic Programming Guide](../vs140/Visual-Basic-Programming-Guide.md)   
 [Assemblies and the Global Assembly Cache (Visual Basic)](../vs140/Assemblies-and-the-Global-Assembly-Cache--Visual-Basic-.md)   
 [Loading Assemblies into an Application Domain](assetId:///1432aa2d-bd83-4346-bf3b-a1b7920e2aa9)