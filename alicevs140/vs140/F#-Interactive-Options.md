---
title: "F# Interactive Options"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 55bf9504-1402-4707-a88d-34f4f8904365
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# F# Interactive Options
This topic describes the command-line options supported by F# Interactive, `fsi.exe`. F# Interactive accepts many of the same command line options as the F# compiler, but also accepts some additional options.  
  
## Using F# Interactive for Scripting  
 F# Interactive, fsi.exe, can be launched interactively, or it can be launched from the command line to run a script. The command line syntax is  
  
 `fsi.exe` [`options`] [`script-file` [`arguments`] ]  
  
 The file extension for F# script files is `fsx`.  
  
## Table of F# Interactive Options  
 The following table summarizes the options supported by F# Interactive. You can set these options on the command-line or through the Visual Studio IDE. To set these options in the Visual Studio IDE, open the **Tools** menu, select **Options...**, then expand the **F# Tools** node and select **F# Interactive**.  
  
 Where lists appear in F# Interactive option arguments, list elements are separated by semicolons (`;`).  
  
|Option|Description|  
|------------|-----------------|  
|`--`|Used to instruct F# Interactive to treat remaining arguments as command line arguments to the F# program or script, which you can access in code by using the list `fsi.CommandLineArgs`.|  
|`--checked`[`+`&#124;`-`]|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--codepage:<int>`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--crossoptimize`[`+`&#124;`-`]|Enable or disable cross-module optimizations.|  
|`--debug`[`+`&#124;`-`]<br /><br /> `--debug:`[`full`&#124;`pdbonly`]<br /><br /> `-g`[`+`&#124;`-`]<br /><br /> `-g:`[`full`&#124;`pdbonly`]|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--define:<string>`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--exec`|Instructs F# interactive to exit after loading the files or running the script file given on the command line.|  
|`--fullpaths`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--gui`[`+`&#124;`-`]|Enables or disables the Windows Forms event loop. The default is enabled.|  
|`--help`<br /><br /> `-?`|Used to display the command line syntax and a brief description of each option.|  
|`--lib:<folder-list>`<br /><br /> `-I:<folder-list>`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--load:<filename>`|Compiles the given source code at startup and loads the compiled F# constructs into the session. If the target source contains scripting directives such as `#use` or `#load`, then you must use `--use` or `#use` instead of `--load` or `#load`.|  
|`--mlcompatibility`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--noframework`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md)|  
|`--nologo`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--nowarn:<warning-list>`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--optimize`[`+`&#124;`-`]|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--quiet`|Suppress F# Interactive's output to the `stdout` stream.|  
|`--quotations-debug`|Specifies that extra debugging information should be emitted for expressions that are derived from F# quotation literals and reflected definitions. The debug information is added to the custom attributes of an F# expression tree node. See [Code Quotations](../vs140/Code-Quotations--F#-.md) and [Expr.CustomAttributes](../vs140/Expr.CustomAttributes-Property--F#-.md).|  
|`--readline`[`+`&#124;`-`]|Enable or disable tab completion in interactive mode.|  
|`--reference:<filename>`<br /><br /> `-r:<filename>`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--tailcalls`[`+`&#124;`-`]|Enable or disable the use of the tail IL instruction, which causes the stack frame to be reused for tail recursive functions. This option is enabled by default.|  
|`--use:<filename>`|Tells the interpreter to use the given file on startup as initial input.|  
|`--utf8output`|Same as the fsc.exe compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--warn:<warning-level>`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--warnaserror`[`+`&#124;`-`]|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
|`--warnaserror`[`+`&#124;`-`]:`<int-list>`|Same as the `fsc.exe` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).|  
  
## Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[Compiler Options (F#)](../vs140/Compiler-Options--F#-.md)|Describes command line options available for the F# compiler, `fsc.exe`.|