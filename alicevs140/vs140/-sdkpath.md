---
title: "-sdkpath"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
H1: /sdkpath
ms.assetid: fec8a3f1-b791-4a37-8af7-344859f8212d
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -sdkpath
Specifies the location of Mscorlib.dll and Microsoft.VisualBasic.dll.  
  
## Syntax  
  
```  
/sdkpath:path  
```  
  
## Arguments  
 `path`  
 The directory containing the versions of Mscorlib.dll and Microsoft.VisualBasic.dll to use for compilation. This path is not verified until it is loaded. Enclose the directory name in quotation marks (" ") if it contains a space.  
  
## Remarks  
 This option tells the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler to load the Mscorlib.dll and Microsoft.VisualBasic.dll files from a non-default location. The `/sdkpath` option was designed to be used with [/netcf](../vs140/-netcf.md). The [!INCLUDE[Compact](../vs140/includes/compact_md.md)] uses different versions of these support libraries to avoid the use of types and language features not found on the devices.  
  
> [!NOTE]
>  The `/sdkpath` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line. The `/sdkpath` option is set when a [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] device project is loaded.  
  
 You can specify that the compiler should compile without a reference to the Visual Basic Runtime Library by using the `/vbruntime` compiler option. For more information, see [/vbruntime](../Topic/-vbruntime.md).  
  
## Example  
 The following code compiles `Myfile.vb` with the [!INCLUDE[Compact](../vs140/includes/compact_md.md)], using the versions of Mscorlib.dll and Microsoft.VisualBasic.dll found in the default installation directory of the [!INCLUDE[Compact](../vs140/includes/compact_md.md)] on the C drive. Typically, you would use the most recent version of the [!INCLUDE[Compact](../vs140/includes/compact_md.md)].  
  
```  
vbc /netcf /sdkpath:"c:\Program Files\Microsoft Visual Studio .NET 2003\CompactFrameworkSDK\v1.0.5000\Windows CE " myfile.vb  
```  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)   
 [/netcf](../vs140/-netcf.md)   
 [/vbruntime](../Topic/-vbruntime.md)