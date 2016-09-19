---
title: "C# Compiler Options Listed by Category"
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
ms.assetid: 96437ecc-6502-4cd3-b070-e9386a298e83
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C# Compiler Options Listed by Category
The following compiler options are sorted by category. For an alphabetical list, see [C# Compiler Options Listed Alphabetically](../vs140/C#-Compiler-Options-Listed-Alphabetically.md).  
  
### Optimization  
  
|Option|Purpose|  
|------------|-------------|  
|[/filealign](../Topic/-filealign%20\(C%23%20Compiler%20Options\).md)|Specifies the size of sections in the output file.|  
|[/optimize](../vs140/-optimize--C#-Compiler-Options-.md)|Enables/disables optimizations.|  
  
### Output Files  
  
|Option|Purpose|  
|------------|-------------|  
|[/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md)|Specifies an XML file where processed documentation comments are to be written.|  
|[/out](../Topic/-out%20\(C%23%20Compiler%20Options\).md)|Specifies the output file.|  
|[/pdb](../vs140/-pdb--C#-Compiler-Options-.md)|Specifies the file name and location of the .pdb file.|  
|[/platform](../Topic/-platform%20\(C%23%20Compiler%20Options\).md)|Specify the output platform.|  
|[/preferreduilang](../vs140/-preferreduilang--C#-Compiler-Options-.md)|Specify a language for compiler output.|  
|[/target](../Topic/-target%20\(C%23%20Compiler%20Options\).md)|Specifies the format of the output file using one of five options: [/target:appcontainerexe](../Topic/-target:appcontainerexe%20\(C%23%20Compiler%20Options\).md), [/target:exe](../vs140/-target-exe--C#-Compiler-Options-.md), [/target:library](../vs140/-target-library--C#-Compiler-Options-.md), [/target:module](../vs140/-target-module--C#-Compiler-Options-.md), [/target:winexe](../Topic/-target:winexe%20\(C%23%20Compiler%20Options\).md), or [/target:winmdobj](../vs140/-target-winmdobj--C#-Compiler-Options-.md).|  
|`/modulename:<string>`|Specify the name of the source module|  
  
### .NET Framework Assemblies  
  
|Option|Purpose|  
|------------|-------------|  
|[/addmodule](../Topic/-addmodule%20\(C%23%20Compiler%20Options\).md)|Specifies one or more modules to be part of this assembly.|  
|[/delaysign](../Topic/-delaysign%20\(C%23%20Compiler%20Options\).md)|Instructs the compiler to add the public key but to leave the assembly unsigned.|  
|[/keycontainer](../Topic/-keycontainer%20\(C%23%20Compiler%20Options\).md)|Specifies the name of the cryptographic key container.|  
|[/keyfile](../Topic/-keyfile%20\(C%23%20Compiler%20Options\).md)|Specifies the filename containing the cryptographic key.|  
|[/lib](../vs140/-lib--C#-Compiler-Options-.md)|Specifies the location of assemblies referenced by means of [/reference](../vs140/-reference--C#-Compiler-Options-.md).|  
|[/nostdlib](../Topic/-nostdlib%20\(C%23%20Compiler%20Options\).md)|Instructs the compiler not to import the standard library (mscorlib.dll).|  
|[/reference](../vs140/-reference--C#-Compiler-Options-.md)|Imports metadata from a file that contains an assembly.|  
|`/analyzer`|Run the analyzers from this assembly (Short form: /a)|  
|`/additionalfile`|Names additional files that don't directly affect code generation but may be used by analyzers for producing errors or warnings.|  
  
### Debugging/Error Checking  
  
|Option|Purpose|  
|------------|-------------|  
|[/bugreport](../vs140/-bugreport--C#-Compiler-Options-.md)|Creates a file that contains information that makes it easy to report a bug.|  
|[/checked](../Topic/-checked%20\(C%23%20Compiler%20Options\).md)|Specifies whether integer arithmetic that overflows the bounds of the data type will cause an exception at run time.|  
|[/debug](../Topic/-debug%20\(C%23%20Compiler%20Options\).md)|Instruct the compiler to emit debugging information.|  
|[/errorreport](../Topic/-errorreport%20\(C%23%20Compiler%20Options\).md)|Sets error reporting behavior.|  
|[/fullpaths](../vs140/-fullpaths--C#-Compiler-Options-.md)|Specifies the absolute path to the file in compiler output.|  
|[/nowarn](../vs140/-nowarn--C#-Compiler-Options-.md)|Suppresses the compiler's generation of specified warnings.|  
|[/warn](../vs140/-warn--C#-Compiler-Options-.md)|Sets the warning level.|  
|[/warnaserror](../Topic/-warnaserror%20\(C%23%20Compiler%20Options\).md)|Promotes warnings to errors.|  
|`/ruleset:<file>`|Specify a ruleset file that disables specific diagnostics.|  
  
### Preprocessor  
  
|Option|Purpose|  
|------------|-------------|  
|[/define](../Topic/-define%20\(C%23%20Compiler%20Options\).md)|Defines preprocessor symbols.|  
  
### Resources  
  
|Option|Purpose|  
|------------|-------------|  
|[/link](../Topic/-link%20\(C%23%20Compiler%20Options\).md)|Makes COM type information in specified assemblies available to the project.|  
|[/linkresource](../Topic/-linkresource%20\(C%23%20Compiler%20Options\).md)|Creates a link to a managed resource.|  
|[/resource](../Topic/-resource%20\(C%23%20Compiler%20Options\).md)|Embeds a .NET Framework resource into the output file.|  
|[/win32icon](../vs140/-win32icon--C#-Compiler-Options-.md)|Specifies an .ico file to insert into the output file.|  
|[/win32res](../vs140/-win32res--C#-Compiler-Options-.md)|Specifies a Win32 resource to insert into the output file.|  
  
### Miscellaneous  
  
|Option|Purpose|  
|------------|-------------|  
|[@](../vs140/@--C#-Compiler-Options-.md)|Specifies a response file.|  
|[/?](../vs140/-help------C#-Compiler-Options-.md)|Lists compiler options to stdout.|  
|[/baseaddress](../Topic/-baseaddress%20\(C%23%20Compiler%20Options\).md)|Specifies the preferred base address at which to load a DLL.|  
|[/codepage](../vs140/-codepage--C#-Compiler-Options-.md)|Specifies the code page to use for all source code files in the compilation.|  
|[/help](../vs140/-help------C#-Compiler-Options-.md)|Lists compiler options to stdout.|  
|[/highentropyva](../vs140/-highentropyva--C#-Compiler-Options-.md)|Specifies that the executable file supports address space layout randomization (ASLR).|  
|[/langversion](../Topic/-langversion%20\(C%23%20Compiler%20Options\).md)|Specify language version mode: ISO-1, ISO-2, 3, 4, 5, 6, or Default|  
|[/main](../Topic/-main%20\(C%23%20Compiler%20Options\).md)|Specifies the location of the **Main** method.|  
|[/noconfig](../vs140/-noconfig--C#-Compiler-Options-.md)|Instructs the compiler not to compile with csc.rsp.|  
|[/nologo](../vs140/-nologo--C#-Compiler-Options-.md)|Suppresses compiler banner information.|  
|[/recurse](../vs140/-recurse--C#-Compiler-Options-.md)|Searches subdirectories for source files to compile.|  
|[/subsystemversion](../vs140/-subsystemversion--C#-Compiler-Options-.md)|Specifies the minimum version of the subsystem that the executable file can use.|  
|[/unsafe](../Topic/-unsafe%20\(C%23%20Compiler%20Options\).md)|Enables compilation of code that uses the [unsafe](../vs140/unsafe--C#-Reference-.md) keyword.|  
|[/utf8output](../vs140/-utf8output--C#-Compiler-Options-.md)|Displays compiler output using UTF-8 encoding.|  
|`/parallel[+&#124;-]`|Specifies whether to use concurrent build (+).|  
|`/checksumalgorithm:<alg>`|Specify the algorithm for calculating the source file checksum stored in PDB.  Supported values are: SHA1 (default) or SHA256.|  
  
## Obsolete Options  
  
|||  
|-|-|  
|**/incremental**|Enables incremental compilation.|  
  
## See Also  
 [C# Compiler Options](../vs140/C#-Compiler-Options.md)   
 [C# Compiler Options Listed Alphabetically](../vs140/C#-Compiler-Options-Listed-Alphabetically.md)   
 [How to: Set Environment Variables for the Visual Studio Command Line](../vs140/How-to--Set-Environment-Variables-for-the-Visual-Studio-Command-Line.md)