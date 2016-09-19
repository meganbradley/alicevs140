---
title: "-LTCG (Link-time Code Generation)"
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
H1: /LTCG (Link-time Code Generation)
ms.assetid: 788c6f52-fdb8-40c2-90af-4026ea2cf2e2
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -LTCG (Link-time Code Generation)
```  
/LTCG[:INCREMENTAL|:NOSTATUS|:STATUS|:OFF|:PGINSTRUMENT|:PGOPTIMIZE|:PGUPDATE]  
```  
  
## Remarks  
 :INCREMENTAL (optional)  
 Specifies that the linker only applies whole program optimization or link-time code generation (LTCG) to the set of files affected by an edit, instead of the entire project. By default, this flag is not set when /LTCG is specified, and the entire project is linked by using whole program optimization.  
  
 :NOSTATUS &#124; :STATUS (optional)  
 Specifies whether the linker displays a progress indicator that shows what percentage of the link is complete. By default, this status information is not displayed.  
  
 :OFF (optional)  
 Disables link-time code generation. This behavior is the same as when /LTCG is not specified on the command line.  
  
 :PGINSTRUMENT (optional)  
 This option is deprecated. Instead, use **/LTCG** and  **/GENPROFILE** or **/FASTGENPROFILE** to generate an instrumented build for profile-guided optimization.  
  
 The data that is collected from instrumented runs is used to create an optimized image. For more information, see [Profile Guided Optimization](../vs140/Profile-Guided-Optimizations.md). The short form of this option is /LTCG:PGI.  
  
 :PGOPTIMIZE (optional)  
 This option is deprecated. Instead, use **/LTCG** and  **/USEPROFILE** to build an optimized image. For more information, see [Profile Guided Optimization](../vs140/Profile-Guided-Optimizations.md). The short form of this option is /LTCG:PGO.  
  
 :PGUPDATE (optional)  
 This option is deprecated. Instead, use **/LTCG** and  **/USEPROFILE** to build an optimized image. For more information, see [Profile Guided Optimization](../vs140/Profile-Guided-Optimizations.md). The short form of this option is /LTCG:PGU.  
  
 The /LTCG option tells the linker to call the compiler and perform whole-program optimization. You can also do profile guided optimization. For more information, see [Profile Guided Optimization](../vs140/Profile-Guided-Optimizations.md).  
  
 With the following exceptions, you cannot add linker options to the PGO combination of /LTCG and /USEPROFILE that were not specified in the previous PGO initialization combination of  /LTCG and /GENPROFILE options:  
  
-   [/BASE](../Topic/-BASE%20\(Base%20Address\).md)  
  
-   [/FIXED](../Topic/-FIXED%20\(Fixed%20Base%20Address\).md)  
  
-   /LTCG  
  
-   [/MAP](../vs140/-MAP--Generate-Mapfile-.md)  
  
-   [/MAPINFO](../vs140/-MAPINFO--Include-Information-in-Mapfile-.md)  
  
-   [/NOLOGO](../vs140/-NOLOGO--Suppress-Startup-Banner---Linker-.md)  
  
-   [/OUT](../vs140/-OUT--Output-File-Name-.md)  
  
-   [/PGD](../vs140/-PGD--Specify-Database-for-Profile-Guided-Optimizations-.md)  
  
-   [/PDB](../vs140/-PDB--Use-Program-Database-.md)  
  
-   [/PDBSTRIPPED](../vs140/-PDBSTRIPPED--Strip-Private-Symbols-.md)  
  
-   [/STUB](../vs140/-STUB--MS-DOS-Stub-File-Name-.md)  
  
-   [/VERBOSE](../vs140/-VERBOSE--Print-Progress-Messages-.md)  
  
 Any linker options that are specified together with the /LTCG and /GENPROFILE options to initialize PGO do not have to be specified when you build by using /LTCG and /USEPROFILE; they are implied.  
  
 The rest of this topic discusses /LTCG in terms of link-time code generation.  
  
 /LTCG is implied with [/GL](../Topic/-GL%20\(Whole%20Program%20Optimization\).md).  
  
 The linker invokes link-time code generation if it is passed a module that was compiled by using **/GL** or an MSIL module (see [.netmodule Files as Linker Input](../vs140/.netmodule-Files-as-Linker-Input.md)). If you do not explicitly specify **/LTCG** when you pass **/GL** or MSIL modules to the linker, the linker eventually detects this and restarts the link by using **/LTCG**. Explicitly specify **/LTCG** when you pass **/GL** and MSIL modules to the linker for the fastest possible build performance.  
  
 For even faster performance, use **/LTCG:INCREMENTAL**. This option tells the linker to only re-optimize the set of files that is affected by a source file change, instead of the entire project. This can significantly reduce the link time required. This is not the same option as incremental linking.  
  
 **/LTCG** is not valid for use with [/INCREMENTAL](../Topic/-INCREMENTAL%20\(Link%20Incrementally\).md).  
  
 When **/LTCG** is used to link modules compiled by using [/Og](../vs140/-Og--Global-Optimizations-.md), [/O1](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md), [/O2](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md), or [/Ox](../vs140/-Ox--Full-Optimization-.md), the following optimizations are performed:  
  
-   Cross-module inlining  
  
-   Interprocedural register allocation (64-bit operating systems only)  
  
-   Custom calling convention (x86 only)  
  
-   Small TLS displacement (x86 only)  
  
-   Stack double alignment (x86 only)  
  
-   Improved memory disambiguation (better interference information for global variables and input parameters)  
  
> [!NOTE]
>  The linker determines which optimizations were used to compile each function and applies the same optimizations at link time.  
  
 Using **/LTCG** and **/Ogt** causes double-alignment optimization.  
  
 If **/LTCG** and **/Ogs** are specified, double alignment is not performed. If most of the functions in an application are compiled for speed, with a few functions compiled for size (for example, by using the [optimize](../vs140/optimize.md) pragma), the compiler double-aligns the functions that are optimized for size if they call functions that require double alignment.  
  
 If the compiler can identify all of the call sites of a function, the compiler ignores explicit calling-convention modifiers on a function and tries to optimize the function's calling convention:  
  
-   pass parameters in registers  
  
-   reorder parameters for alignment  
  
-   remove unused parameters  
  
 If a function is called through a function pointer, or if a function is called from outside a module that is compiled by using **/GL**, the compiler does not attempt to optimize the function's calling convention.  
  
> [!NOTE]
>  If you use **/LTCG** and redefine mainCRTStartup, your application can have unpredictable behavior that relates to user code that executes before global objects are initialized.  There are three ways to address this issue: do not redefine mainCRTStartup, do not compile the file that contains mainCRTStartup by using **/LTCG**, or initialize global variables and objects statically.  
  
## /LTCG and MSIL Modules  
 Modules that are compiled by using [/GL](../Topic/-GL%20\(Whole%20Program%20Optimization\).md) and [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) can be used as input to the linker when **/LTCG** is specified.  
  
-   **/LTCG** can accept native object files, mixed native/managed object files (compiled by using **/clr**), and pure object files (compiled by using **/clr:pure**), and safe object files (compiled by using **/clr:safe**)  
  
-   **/LTCG** can accept safe .netmodules, which can be created by using **/clr:safe /LN** in Visual C++ and **/target:module** in any other Visual Studio compiler. .Netmodules produced by using**/clr** or **/clr:pure** are not accepted by **/LTCG**.  
  
-   /LTCG:PGI does not accept native modules compiled by using **/GL** and **/clr**, or pure modules (produced by using **/clr:pure**)  
  
#### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project **Property Pages** dialog box. See [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Select the **Configuration Properties** folder.  
  
3.  Select the **General** property page.  
  
4.  Modify the **Whole Program Optimization** property.  
  
 You can also apply **/LTCG** to specific builds by choosing **Build**, **Profile Guided Optimization** on the menu bar, or by choosing one of the Profile Guided Optimization options on the shortcut menu for the project.  
  
#### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.LinkTimeCodeGeneration?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)