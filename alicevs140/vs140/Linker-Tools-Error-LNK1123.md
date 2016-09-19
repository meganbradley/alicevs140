---
title: "Linker Tools Error LNK1123"
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
ms.topic: error-reference
ms.assetid: fe47af69-0f42-4792-9133-541192cd8514
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1123
failure during conversion to COFF: file invalid or corrupt  
  
 Input files must have the Common Object File Format (COFF) format. If an input file is not COFF, the linker automatically tries to convert 32-bit OMF objects to COFF, or runs CVTRES.EXE to convert resource files. This message indicates that the linker could not convert the file. This can also occur when using an incompatible version of CVTRES.EXE from another installation of Visual Studio, the Windows Development Kit, or .NET Framework.  
  
> [!NOTE]
>  If you are running an earlier version of Visual Studio, automatic conversion may not be supported.  
  
### To fix the problem  
  
-   Apply all service packs and updates for your version of Visual Studio. This is particularly important for Visual Studio 2010.  
  
-   Try building with incremental linking disabled. On the menu bar, choose **Project**, **Properties**. In the **Property Pages** dialog box, expand **Configuration Properties**, **Linker**. Change the value of **Enable Incremental Linking** to **No**.  
  
-   Verify that the version of CVTRES.EXE found first in your PATH environment variable matches the version of the build tools, or the version of the Platform Toolset, used by your project.  
  
-   Try turning off the Embed Manifest option. On the menu bar, choose **Project**, **Properties**. In the **Property Pages** dialog box, expand **Configuration Properties**, **Manifest Tool**, **Input and Output**. Change the value of **Embed Manifest** to **No**.  
  
-   Make sure that the file type is valid. For example, make sure that an OMF object is 32-bit and not 16-bit. For more information, see [.Obj Files as Linker Input](../vs140/.Obj-Files-as-Linker-Input.md) and [Microsoft PE and COFF Specification](http://go.microsoft.com/fwlink/p/?LinkId=93292).  
  
-   Make sure that the file is not corrupt. Rebuild it, if necessary.  
  
## See Also  
 [.Obj Files as Linker Input](../vs140/.Obj-Files-as-Linker-Input.md)   
 [EDITBIN Reference](../vs140/EDITBIN-Reference.md)   
 [DUMPBIN Reference](../vs140/DUMPBIN-Reference.md)