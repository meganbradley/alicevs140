---
title: "C# Compiler Options Listed Alphabetically"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 43535ea0-ca47-4a15-b528-615087a86092
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C# Compiler Options Listed Alphabetically
The following compiler options are sorted alphabetically. For a categorical list, see [C# Compiler Options Listed by Category](../vs140/C#-Compiler-Options-Listed-by-Category.md).  
  
|Option|Purpose|  
|------------|-------------|  
|[@](../vs140/@--C#-Compiler-Options-.md)|Reads a response file for more options.|  
|[/?](../vs140/-help------C#-Compiler-Options-.md)|Displays a usage message to stdout.|  
|`/additionalfile`|Names additional files that don't directly affect code generation but may be used by analyzers for producing errors or warnings.|  
|[/addmodule](../Topic/-addmodule%20\(C%23%20Compiler%20Options\).md)|Links the specified modules into this assembly|  
|`/analyzer`|Run the analyzers from this assembly (Short form: /a)|  
|[/appconfig](../vs140/-appconfig--C#-Compiler-Options-.md)|Specifies the location of app.config at assembly binding time.|  
|[/baseaddress](../Topic/-baseaddress%20\(C%23%20Compiler%20Options\).md)|Specifies the base address for the library to be built.|  
|[/bugreport](../vs140/-bugreport--C#-Compiler-Options-.md)|Creates a 'Bug Report' file. This file will be sent together with any crash information if it is used with **/errorreport:prompt** or **/errorreport:send**.|  
|[/checked](../Topic/-checked%20\(C%23%20Compiler%20Options\).md)|Causes the compiler to generate overflow checks.|  
|`/checksumalgorithm:<alg>`|Specify the algorithm for calculating the source file checksum stored in PDB.  Supported values are: SHA1 (default) or SHA256.|  
|[/codepage](../vs140/-codepage--C#-Compiler-Options-.md)|Specifies the codepage to use when opening source files.|  
|[/debug](../Topic/-debug%20\(C%23%20Compiler%20Options\).md)|Emits debugging information.|  
|[/define](../Topic/-define%20\(C%23%20Compiler%20Options\).md)|Defines conditional compilation symbols.|  
|[/delaysign](../Topic/-delaysign%20\(C%23%20Compiler%20Options\).md)|Delay-signs the assembly by using only the public part of the strong name key.|  
|[/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md)|Specifies an XML Documentation file to generate.|  
|[/errorreport](../Topic/-errorreport%20\(C%23%20Compiler%20Options\).md)|Specifies how to handle internal compiler errors: prompt, send, or none. The default is none.|  
|[/filealign](../Topic/-filealign%20\(C%23%20Compiler%20Options\).md)|Specifies the alignment used for output file sections.|  
|[/fullpaths](../vs140/-fullpaths--C#-Compiler-Options-.md)|Causes the compiler to generate fully qualified paths.|  
|[/help](../vs140/-help------C#-Compiler-Options-.md)|Displays a usage message to stdout.|  
|[/highentropyva](../vs140/-highentropyva--C#-Compiler-Options-.md)|Specifies that high entropy ASLR is supported.|  
|**/incremental**|Enables incremental compilation [obsolete].|  
|[/keycontainer](../Topic/-keycontainer%20\(C%23%20Compiler%20Options\).md)|Specifies a strong name key container.|  
|[/keyfile](../Topic/-keyfile%20\(C%23%20Compiler%20Options\).md)|Specifies a strong name key file.|  
|[/langversion:<string\>](../Topic/-langversion%20\(C%23%20Compiler%20Options\).md)|Specify language version mode: ISO-1, ISO-2, 3, 4, 5, 6, or Default|  
|[/lib](../vs140/-lib--C#-Compiler-Options-.md)|Specifies additional directories in which to search for references.|  
|[/link](../Topic/-link%20\(C%23%20Compiler%20Options\).md)|Makes COM type information in specified assemblies available to the project.|  
|[/linkresource](../Topic/-linkresource%20\(C%23%20Compiler%20Options\).md)|Links the specified resource to this assembly.|  
|[/main](../Topic/-main%20\(C%23%20Compiler%20Options\).md)|Specifies the type that contains the entry point (ignore all other possible entry points).|  
|[/moduleassemblyname](../vs140/-moduleassemblyname--C#-Compiler-Option-.md)|Specifies an assembly whose non-public types a .netmodule can access.|  
|`/modulename:<string>`|Specify the name of the source module|  
|[/noconfig](../vs140/-noconfig--C#-Compiler-Options-.md)|Instructs the compiler not to auto include CSC.RSP file.|  
|[/nologo](../vs140/-nologo--C#-Compiler-Options-.md)|Suppresses compiler copyright message.|  
|[/nostdlib](../Topic/-nostdlib%20\(C%23%20Compiler%20Options\).md)|Instructs the compiler not to reference standard library (mscorlib.dll).|  
|[/nowarn](../vs140/-nowarn--C#-Compiler-Options-.md)|Disables specific warning messages|  
|[/nowin32manifest](../vs140/-nowin32manifest--C#-Compiler-Options-.md)|Instructs the compiler not to embed an application manifest in the executable file.|  
|[/optimize](../vs140/-optimize--C#-Compiler-Options-.md)|Enables/disables optimizations.|  
|[/out](../Topic/-out%20\(C%23%20Compiler%20Options\).md)|Specifies the output file name (default: base name of file with main class or first file).|  
|`/parallel[+&#124;-]`|Specifies whether to use concurrent build (+).|  
|[/pdb](../vs140/-pdb--C#-Compiler-Options-.md)|Specifies the file name and location of the .pdb file.|  
|[/platform](../Topic/-platform%20\(C%23%20Compiler%20Options\).md)|Limits which platforms this code can run on: x86, Itanium, x64, anycpu, or anycpu32bitpreferred. The default is anycpu.|  
|[/preferreduilang](../vs140/-preferreduilang--C#-Compiler-Options-.md)|Specifies the language to be used for compiler output.|  
|[/recurse](../vs140/-recurse--C#-Compiler-Options-.md)|Includes all files in the current directory and subdirectories according to the wildcard specifications.|  
|[/reference](../vs140/-reference--C#-Compiler-Options-.md)|References metadata from the specified assembly files.|  
|[/resource](../Topic/-resource%20\(C%23%20Compiler%20Options\).md)|Embeds the specified resource.|  
|`/ruleset:<file>`|Specify a ruleset file that disables specific diagnostics.|  
|[/subsystemversion](../vs140/-subsystemversion--C#-Compiler-Options-.md)|Specifies the minimum version of the subsystem that the executable file can use.|  
|[/target](../Topic/-target%20\(C%23%20Compiler%20Options\).md)|Specifies the format of the output file by using one of four options:[/target:appcontainerexe](../Topic/-target:appcontainerexe%20\(C%23%20Compiler%20Options\).md), [/target:exe](../vs140/-target-exe--C#-Compiler-Options-.md), [/target:library](../vs140/-target-library--C#-Compiler-Options-.md), [/target:module](../vs140/-target-module--C#-Compiler-Options-.md), [/target:winexe](../Topic/-target:winexe%20\(C%23%20Compiler%20Options\).md),  [/target:winmdobj](../vs140/-target-winmdobj--C#-Compiler-Options-.md).|  
|[/unsafe](../Topic/-unsafe%20\(C%23%20Compiler%20Options\).md)|Allows [unsafe](../vs140/unsafe--C#-Reference-.md) code.|  
|[/utf8output](../vs140/-utf8output--C#-Compiler-Options-.md)|Outputs compiler messages in UTF-8 encoding.|  
|[/warn](../vs140/-warn--C#-Compiler-Options-.md)|Sets the warning level (0-4).|  
|[/warnaserror](../Topic/-warnaserror%20\(C%23%20Compiler%20Options\).md)|Reports specific warnings as errors.|  
|[/win32icon](../vs140/-win32icon--C#-Compiler-Options-.md)|Uses this icon for the output.|  
|[/win32manifest](../vs140/-win32manifest--C#-Compiler-Options-.md)|Specifies a custom win32 manifest file.|  
|[/win32res](../vs140/-win32res--C#-Compiler-Options-.md)|Specifies the win32 resource file (.res).|  
  
## See Also  
 [C# Compiler Options](../vs140/C#-Compiler-Options.md)   
 [C# Compiler Options Listed by Category](../vs140/C#-Compiler-Options-Listed-by-Category.md)   
 [How to: Set Environment Variables for the Visual Studio Command Line](../vs140/How-to--Set-Environment-Variables-for-the-Visual-Studio-Command-Line.md)   
 [<compiler\> Element](assetId:///7a151659-b803-4c27-b5ce-1c4aa0d5a823)