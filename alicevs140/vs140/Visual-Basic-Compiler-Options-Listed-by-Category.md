---
title: "Visual Basic Compiler Options Listed by Category"
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
ms.assetid: fbe36f7a-7cfa-4f77-a8d4-2be5958568e3
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Visual Basic Compiler Options Listed by Category
The [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] command-line compiler is provided as an alternative to compiling programs from within the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] integrated development environment (IDE). The following is a list of the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] command-line compiler options sorted by functional category.  
  
## Compiler Output  
  
|||  
|-|-|  
|Option|Purpose|  
|[/nologo](../vs140/-nologo--Visual-Basic-.md)|Suppresses compiler banner information.|  
|[/utf8output](../vs140/-utf8output--Visual-Basic-.md)|Displays compiler output using UTF-8 encoding.|  
|[/verbose](../vs140/-verbose.md)|Outputs extra information during compilation.|  
|`/modulename:<string>`|Specify the name of the source module|  
|[/preferreduilang](../vs140/-preferreduilang--C#-Compiler-Options-.md)|Specify a language for compiler output.|  
  
## Optimization  
  
|||  
|-|-|  
|Option|Purpose|  
|[/filealign](../vs140/-filealign.md)|Specifies where to align the sections of the output file.|  
|[/optimize](../vs140/-optimize.md)|Enables/disables optimizations.|  
  
## Output Files  
  
|||  
|-|-|  
|Option|Purpose|  
|[/doc](../vs140/-doc.md)|Process documentation comments to an XML file.|  
|[/netcf](../vs140/-netcf.md)|Sets the compiler to target the [!INCLUDE[Compact](../vs140/includes/compact_md.md)].|  
|[/out](../vs140/-out--Visual-Basic-.md)|Specifies an output file.|  
|[/target](../Topic/-target%20\(Visual%20Basic\).md)|Specifies the format of the output.|  
  
## .NET Assemblies  
  
|||  
|-|-|  
|Option|Purpose|  
|[/addmodule](../vs140/-addmodule.md)|Causes the compiler to make all type information from the specified file(s) available to the project you are currently compiling.|  
|[/delaysign](../vs140/-delaysign.md)|Specifies whether the assembly will be fully or partially signed.|  
|[/imports](../vs140/-imports--Visual-Basic-.md)|Imports a namespace from a specified assembly.|  
|[/keycontainer](../Topic/-keycontainer.md)|Specifies a key container name for a key pair to give an assembly a strong name.|  
|[/keyfile](../vs140/-keyfile.md)|Specifies a file containing a key or key pair to give an assembly a strong name.|  
|[/libpath](../vs140/-libpath.md)|Specifies the location of assemblies referenced by the [/reference](../vs140/-reference--Visual-Basic-.md) option.|  
|[/reference](../vs140/-reference--Visual-Basic-.md)|Imports metadata from an assembly.|  
|[/moduleassemblyname](../vs140/-moduleassemblyname.md)|Specifies the name of the assembly that a module will be a part of.|  
|`/analyzer`|Run the analyzers from this assembly (Short form: /a)|  
|`/additionalfile`|Names additional files that don't directly affect code generation but may be used by analyzers for producing errors or warnings.|  
  
## Debugging/Error Checking  
  
|||  
|-|-|  
|Option|Purpose|  
|[/bugreport](../vs140/-bugreport.md)|Creates a file that contains information that makes it easy to report a bug.|  
|[/debug](../vs140/-debug--Visual-Basic-.md)|Produces debugging information.|  
|[/nowarn](../vs140/-nowarn.md)|Suppresses the compiler's ability to generate warnings.|  
|[/quiet](../vs140/-quiet.md)|Prevents the compiler from displaying code for syntax-related errors and warnings.|  
|[/removeintchecks](../vs140/-removeintchecks.md)|Disables integer overflow checking.|  
|[/warnaserror](../vs140/-warnaserror--Visual-Basic-.md)|Promotes warnings to errors.|  
|`/ruleset:<file>`|Specify a ruleset file that disables specific diagnostics.|  
  
## Help  
  
|||  
|-|-|  
|Option|Purpose|  
|[/?](../vs140/-help------Visual-Basic-.md)|Displays the compiler options. This command is the same as specifying the `/help` option. No compilation occurs.|  
|[/help](../vs140/-help------Visual-Basic-.md)|Displays the compiler options. This command is the same as specifying the `/?` option. No compilation occurs.|  
  
## Language  
  
|||  
|-|-|  
|Option|Purpose|  
|[/langversion](../vs140/-langversion--Visual-Basic-.md)|Specify language version: 9&#124;9.0&#124;10&#124;10.0&#124;11&#124;11.0.|  
|[/optionexplicit](../vs140/-optionexplicit.md)|Enforces explicit declaration of variables.|  
|[/optionstrict](../vs140/-optionstrict.md)|Enforces strict type semantics.|  
|[/optioncompare](../vs140/-optioncompare.md)|Specifies whether string comparisons should be binary or use locale-specific text semantics.|  
|[/optioninfer](../vs140/-optioninfer.md)|Enables the use of local type inference in variable declarations.|  
  
## Preprocessor  
  
|||  
|-|-|  
|Option|Purpose|  
|[/define](../vs140/-define--Visual-Basic-.md)|Defines symbols for conditional compilation.|  
  
## Resources  
  
|||  
|-|-|  
|Option|Purpose|  
|[/linkresource](../vs140/-linkresource--Visual-Basic-.md)|Creates a link to a managed resource.|  
|[/resource](../Topic/-resource%20\(Visual%20Basic\).md)|Embeds a managed resource in an assembly.|  
|[/win32icon](../vs140/-win32icon.md)|Inserts an .ico file into the output file.|  
|[/win32resource](../vs140/-win32resource.md)|Inserts a Win32 resource into the output file.|  
  
## Miscellaneous  
  
|||  
|-|-|  
|Option|Purpose|  
|[@ (Specify Response File)](../vs140/@--Specify-Response-File---Visual-Basic-.md)|Specifies a response file.|  
|[/baseaddress](../vs140/-baseaddress.md)|Specifies the base address of a DLL.|  
|[/codepage](../vs140/-codepage--Visual-Basic-.md)|Specifies the code page to use for all source code files in the compilation.|  
|[/errorreport](../vs140/-errorreport.md)|Specifies how the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler should report internal compiler errors.|  
|[/highentropyva](../vs140/-highentropyva--Visual-Basic-.md)|Tells the Windows kernel whether a particular executable supports high entropy Address Space Layout Randomization (ASLR).|  
|[/main](../Topic/-main.md)|Specifies the class that contains the `Sub``Main` procedure to use at startup.|  
|[/noconfig](../vs140/-noconfig.md)|Do not compile with Vbc.rsp|  
|[/nostdlib](../vs140/-nostdlib--Visual-Basic-.md)|Causes the compiler not to reference the standard libraries.|  
|[/nowin32manifest](../vs140/-nowin32manifest--Visual-Basic-.md)|Instructs the compiler not to embed any application manifest into the executable file.|  
|[/platform](../Topic/-platform%20\(Visual%20Basic\).md)|Specifies the processor platform the compiler targets for the output file.|  
|[/recurse](../vs140/-recurse.md)|Searches subdirectories for source files to compile.|  
|[/rootnamespace](../Topic/-rootnamespace.md)|Specifies a namespace for all type declarations.|  
|[/sdkpath](../vs140/-sdkpath.md)|Specifies the location of Mscorlib.dll and Microsoft.VisualBasic.dll.|  
|[/vbruntime](../Topic/-vbruntime.md)|Specifies that the compiler should compile without a reference to the Visual Basic Runtime Library, or with a reference to a specific runtime library.|  
|[/win32manifest](../vs140/-win32manifest--Visual-Basic-.md)|Identifies a user-defined Win32 application manifest file to be embedded into a project's portable executable (PE) file.|  
|`/parallel[+&#124;-]`|Specifies whether to use concurrent build (+).|  
|`/checksumalgorithm:<alg>`|Specify the algorithm for calculating the source file checksum stored in PDB.  Supported values are: SHA1 (default) or SHA256.|  
  
## See Also  
 [Visual Basic Compiler Options Listed Alphabetically](../vs140/Visual-Basic-Compiler-Options-Listed-Alphabetically.md)   
 [Introduction to the Project Designer](assetId:///898dd854-c98d-430c-ba1b-a913ce3c73d7)   
 [C# Compiler Options Listed Alphabetically](../vs140/C#-Compiler-Options-Listed-Alphabetically.md)   
 [C# Compiler Options Listed by Category](../vs140/C#-Compiler-Options-Listed-by-Category.md)