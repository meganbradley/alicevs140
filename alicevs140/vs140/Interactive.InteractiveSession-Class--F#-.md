---
title: "Interactive.InteractiveSession Class (F#)"
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
ms.assetid: 2f6aa29c-7fb9-43ae-a7e3-6720fcb282bf
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Interactive.InteractiveSession Class (F#)
Operations supported by the currently executing F# Interactive session.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Compiler.Interactive  
  
 **Assembly:** FSharp.Compiler.Interactive.Settings (in FSharp.Compiler.Interactive.Settings.dll)  
  
## Syntax  
  
```  
[<Sealed>]  
type InteractiveSession =  
 class  
  member this.AddPrintTransformer : InteractiveSession -> ('T -> obj) -> unit  
  member this.AddPrinter : InteractiveSession -> ('T -> string) -> unit  
  member this.CommandLineArgs :  string []  
  member this.EventLoop :  IEventLoop  
  member this.FloatingPointFormat :  string  
  member this.FormatProvider :  IFormatProvider  
  member this.PrintDepth :  int  
  member this.PrintLength :  int  
  member this.PrintSize :  int  
  member this.PrintWidth :  int  
  member this.ShowDeclarationValues :  bool  
  member this.ShowIEnumerable :  bool  
  member this.ShowProperties :  bool  
  member this.CommandLineArgs : string [] with set :  string []  
  member this.EventLoop : IEventLoop with set :  IEventLoop  
  member this.FloatingPointFormat : string with set :  string  
  member this.FormatProvider : IFormatProvider with set :  IFormatProvider  
  member this.PrintDepth : int with set :  int  
  member this.PrintLength : int with set :  int  
  member this.PrintSize : int with set :  int  
  member this.PrintWidth : int with set :  int  
  member this.ShowDeclarationValues : bool with set :  bool  
  member this.ShowIEnumerable : bool with set :  bool  
  member this.ShowProperties : bool with set :  bool  
 end  
```  
  
## Remarks  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[AddPrinter](../vs140/InteractiveSession.AddPrinter--T--Method--F#-.md)|Registers a printer that controls the output of the interactive session.|  
|[AddPrintTransformer](../vs140/InteractiveSession.AddPrintTransformer--T--Method--F#-.md)|Registers a print transformer that controls the output of the interactive session.|  
|[CommandLineArgs](../Topic/InteractiveSession.CommandLineArgs%20Property%20\(F%23\).md)|The command line arguments after ignoring the arguments relevant to the interactive environment and replacing the first argument with the name of the last script file, if any.|  
|[EventLoop](../vs140/InteractiveSession.EventLoop-Property--F#-.md)|Gets or sets the current event loop being used to process interactions.|  
|[FloatingPointFormat](../vs140/InteractiveSession.FloatingPointFormat-Property--F#-.md)|Gets or sets the floating point format used in the output of the interactive session.|  
|[FormatProvider](../vs140/InteractiveSession.FormatProvider-Property--F#-.md)|Gets or sets the format provider used in the output of the interactive session.|  
|[PrintDepth](../vs140/InteractiveSession.PrintDepth-Property--F#-.md)|Gets or sets the print depth of the interactive session.|  
|[PrintLength](../vs140/InteractiveSession.PrintLength-Property--F#-.md)|Gets or sets the total print length of the interactive session.|  
|[PrintSize](../vs140/InteractiveSession.PrintSize-Property--F#-.md)|Gets or sets the total print size of the interactive session.|  
|[PrintWidth](../vs140/InteractiveSession.PrintWidth-Property--F#-.md)|Gets or sets the print width of the interactive session.|  
|[ShowDeclarationValues](../vs140/InteractiveSession.ShowDeclarationValues-Property--F#-.md)|When set to `false`, disables the display of declaration values in the output of the interactive session.|  
|[ShowIEnumerable](../vs140/InteractiveSession.ShowIEnumerable-Property--F#-.md)|When set to `false`, disables the display of sequences in the output of the interactive session.|  
|[ShowProperties](../vs140/InteractiveSession.ShowProperties-Property--F#-.md)|When set to `false`, disables the display of properties of evaluated objects in the output of the interactive session.|  
  
## Platforms  
 Windows 7, Windows Vista SP2, Windows XP SP3, Windows XP x64 SP2, Windows Server 2008 R2, Windows Server 2008 SP2, Windows Server 2003 SP2  
  
## Version Information  
 **F# Runtime**  
  
 Supported in: 2.0, 4.0  
  
 **Silverlight**  
  
 Supported in: 2, 3  
  
## See Also  
 [Microsoft.FSharp.Compiler.Interactive Namespace (F#)](../vs140/Microsoft.FSharp.Compiler.Interactive-Namespace--F#-.md)