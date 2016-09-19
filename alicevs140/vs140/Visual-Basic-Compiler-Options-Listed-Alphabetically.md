---
title: "Visual Basic Compiler Options Listed Alphabetically"
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
ms.assetid: e67febba-bacf-4e1f-a143-c141e063f90e
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Visual Basic Compiler Options Listed Alphabetically
The [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] command-line compiler is provided as an alternative to compiling programs from the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] integrated development environment (IDE). The following is a list of the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] command-line compiler options sorted alphabetically.  
  
|Option|Purpose|  
|------------|-------------|  
|[@ (Specify Response File)](../vs140/@--Specify-Response-File---Visual-Basic-.md)|Specifies a response file.|  
|[/?](../vs140/-help------Visual-Basic-.md)|Displays compiler options. This command is the same as specifying the `/help` option. No compilation occurs.|  
|`/additionalfile`|Names additional files that don't directly affect code generation but may be used by analyzers for producing errors or warnings.|  
|[/addmodule](../vs140/-addmodule.md)|Causes the compiler to make all type information from the specified file(s) available to the project you are currently compiling.|  
|`/analyzer`|Run the analyzers from this assembly (Short form: /a)|  
|[/baseaddress](../vs140/-baseaddress.md)|Specifies the base address of a DLL.|  
|[/bugreport](../vs140/-bugreport.md)|Creates a file that contains information that makes it easy to report a bug.|  
|`/checksumalgorithm:<alg>`|Specify the algorithm for calculating the source file checksum stored in PDB.  Supported values are: SHA1 (default) or SHA256.|  
|[/codepage](../vs140/-codepage--Visual-Basic-.md)|Specifies the code page to use for all source code files in the compilation.|  
|[/debug](../vs140/-debug--Visual-Basic-.md)|Produces debugging information.|  
|[/define](../vs140/-define--Visual-Basic-.md)|Defines symbols for conditional compilation.|  
|[/delaysign](../vs140/-delaysign.md)|Specifies whether the assembly will be fully or partially signed.|  
|[/doc](../vs140/-doc.md)|Processes documentation comments to an XML file.|  
|[/errorreport](../vs140/-errorreport.md)|Specifies how the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler should report internal compiler errors.|  
|[/filealign](../vs140/-filealign.md)|Specifies where to align the sections of the output file.|  
|[/help](../vs140/-help------Visual-Basic-.md)|Displays compiler options. This command is the same as specifying the `/?` option. No compilation occurs.|  
|[/highentropyva](../vs140/-highentropyva--Visual-Basic-.md)|Indicates whether a particular executable supports high entropy Address Space Layout Randomization (ASLR).|  
|[/imports](../vs140/-imports--Visual-Basic-.md)|Imports a namespace from a specified assembly.|  
|[/keycontainer](../Topic/-keycontainer.md)|Specifies a key container name for a key pair to give an assembly a strong name.|  
|[/keyfile](../vs140/-keyfile.md)|Specifies a file that contains a key or key pair to give an assembly a strong name.|  
|[/langversion](../vs140/-langversion--Visual-Basic-.md)|Specify language version: 9&#124;9.0&#124;10&#124;10.0&#124;11&#124;11.0.|  
|[/libpath](../vs140/-libpath.md)|Specifies the location of assemblies referenced by the [/reference](../vs140/-reference--Visual-Basic-.md) option.|  
|[/linkresource](../vs140/-linkresource--Visual-Basic-.md)|Creates a link to a managed resource.|  
|[/main](../Topic/-main.md)|Specifies the class that contains the `Sub``Main` procedure to use at startup.|  
|[/moduleassemblyname](../vs140/-moduleassemblyname.md)|Specifies the name of the assembly that a module will be a part of.|  
|`/modulename:<string>`|Specify the name of the source module|  
|[/netcf](../vs140/-netcf.md)|Sets the compiler to target the [!INCLUDE[Compact](../vs140/includes/compact_md.md)].|  
|[/noconfig](../vs140/-noconfig.md)|Do not compile with Vbc.rsp.|  
|[/nologo](../vs140/-nologo--Visual-Basic-.md)|Suppresses compiler banner information.|  
|[/nostdlib](../vs140/-nostdlib--Visual-Basic-.md)|Causes the compiler not to reference the standard libraries.|  
|[/nowarn](../vs140/-nowarn.md)|Suppresses the compiler's ability to generate warnings.|  
|[/nowin32manifest](../vs140/-nowin32manifest--Visual-Basic-.md)|Instructs the compiler not to embed any application manifest into the executable file.|  
|[/optimize](../vs140/-optimize.md)|Enables/disables code optimization.|  
|[/optioncompare](../vs140/-optioncompare.md)|Specifies whether string comparisons should be binary or use locale-specific text semantics.|  
|[/optionexplicit](../vs140/-optionexplicit.md)|Enforces explicit declaration of variables.|  
|[/optioninfer](../vs140/-optioninfer.md)|Enables the use of local type inference in variable declarations.|  
|[/optionstrict](../vs140/-optionstrict.md)|Enforces strict language semantics.|  
|[/out](../vs140/-out--Visual-Basic-.md)|Specifies an output file.|  
|`/parallel[+&#124;-]`|Specifies whether to use concurrent build (+).|  
|[/platform](../Topic/-platform%20\(Visual%20Basic\).md)|Specifies the processor platform the compiler targets for the output file.|  
|`/preferreduilang`|Specify the preferred output language name.|  
|[/quiet](../vs140/-quiet.md)|Prevents the compiler from displaying code for syntax-related errors and warnings.|  
|[/recurse](../vs140/-recurse.md)|Searches subdirectories for source files to compile.|  
|[/reference](../vs140/-reference--Visual-Basic-.md)|Imports metadata from an assembly.|  
|[/removeintchecks](../vs140/-removeintchecks.md)|Disables integer overflow checking.|  
|[/resource](../Topic/-resource%20\(Visual%20Basic\).md)|Embeds a managed resource in an assembly.|  
|[/rootnamespace](../Topic/-rootnamespace.md)|Specifies a namespace for all type declarations.|  
|`/ruleset:<file>`|Specify a ruleset file that disables specific diagnostics.|  
|[/sdkpath](../vs140/-sdkpath.md)|Specifies the location of Mscorlib.dll and Microsoft.VisualBasic.dll.|  
|[/subsystemversion](../vs140/-subsystemversion--Visual-Basic-.md)|Specifies the minimum version of the subsystem that the generated executable file can use.|  
|[/target](../Topic/-target%20\(Visual%20Basic\).md)|Specifies the format of the output file.|  
|[/utf8output](../vs140/-utf8output--Visual-Basic-.md)|Displays compiler output using UTF-8 encoding.|  
|[/vbruntime](../Topic/-vbruntime.md)|Specifies that the compiler should compile without a reference to the Visual Basic Runtime Library, or with a reference to a specific runtime library.|  
|[/verbose](../vs140/-verbose.md)|Outputs extra information during compilation.|  
|[/warnaserror](../vs140/-warnaserror--Visual-Basic-.md)|Promotes warnings to errors.|  
|[/win32icon](../vs140/-win32icon.md)|Inserts an .ico file into the output file.|  
|[/win32manifest](../vs140/-win32manifest--Visual-Basic-.md)|Identifies a user-defined Win32 application manifest file to be embedded into a project's portable executable (PE) file.|  
|[/win32resource](../vs140/-win32resource.md)|Inserts a Win32 resource into the output file.|  
  
## See Also  
 [Visual Basic Compiler Options Listed by Category](../vs140/Visual-Basic-Compiler-Options-Listed-by-Category.md)   
 [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7)   
 [C# Compiler Options Listed Alphabetically](../vs140/C#-Compiler-Options-Listed-Alphabetically.md)   
 [C# Compiler Options Listed by Category](../vs140/C#-Compiler-Options-Listed-by-Category.md)