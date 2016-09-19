---
title: "-ZW (Windows Runtime Compilation)"
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
H1: /ZW (Windows Runtime Compilation)
ms.assetid: 0fe362b0-9526-498b-96e0-00d7a965a248
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -ZW (Windows Runtime Compilation)
Compiles source code to support [!INCLUDE[cppwrt](../vs140/includes/cppwrt_md.md)] ([!INCLUDE[cppwrt_short](../vs140/includes/cppwrt_short_md.md)]) for the creation of [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps.  
  
 When you use **/ZW** to compile, always specify **/EHsc** as well.  
  
## Syntax  
  
```cpp  
/ZW /EHsc  
/ZW:nostdlib /EHsc  
```  
  
## Arguments  
 nostdlib  
 Indicates that Platform.winmd, Windows.Foundation.winmd, and other default Windows metadata (.winmd) files are not automatically included in the compilation. Instead, you must use the [/FU (Name Forced #using File)](../vs140/-FU--Name-Forced-#using-File-.md) compiler option to explicitly specify Windows metadata files.  
  
## Remarks  
 When you specify the **/ZW** option, the compiler supports these features:  
  
-   The required metadata files, namespaces, data types, and functions that your app requires to execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
-   Automatic reference-counting of [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] objects, and automatic discarding of an object when its reference count goes to zero.  
  
 Because the incremental linker does not support the Windows metadata included in .obj files by using the **/ZW** option, the [/Gm](../vs140/-Gm--Enable-Minimal-Rebuild-.md) option is incompatible with **/ZW**.  
  
 For more information, see [Visual C++ Language Reference (C++/CX)](assetId:///3f6abf92-4e5e-4ed8-8e11-f9252380d30a).  
  
## Requirements  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)