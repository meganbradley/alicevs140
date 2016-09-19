---
title: "InteractiveSession.FloatingPointFormat Property (F#)"
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
ms.assetid: 521bfd81-e707-4139-9908-408b7cf64428
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# InteractiveSession.FloatingPointFormat Property (F#)
Gets or sets the floating point format used in the output of the interactive session.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Compiler.Interactive  
  
 **Assembly:** FSharp.Compiler.Interactive.Settings (in FSharp.Compiler.Interactive.Settings.dll)  
  
## Syntax  
  
```  
// Signatures:  
member this.FloatingPointFormat :  string  
member this.FloatingPointFormat : string with set :  string  
  
// Usage:  
interactiveSession.FloatingPointFormat  
interactiveSession.FloatingPointFormat <- floatingPointFormat  
```  
  
#### Parameters  
 `floatingPointFormat`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 A format code to use for floating point output in the F# Interactive Session.  
  
## Return Value  
  
## Remarks  
 The possible format codes are described in [Core.Printf Module (F#)](../Topic/Core.Printf%20Module%20\(F%23\).md). The default value is `g10`.  
  
## Platforms  
 Windows 7, Windows Vista SP2, Windows XP SP3, Windows XP x64 SP2, Windows Server 2008 R2, Windows Server 2008 SP2, Windows Server 2003 SP2  
  
## Version Information  
 **F# Runtime**  
  
 Supported in: 2.0, 4.0  
  
 **Silverlight**  
  
 Supported in: 2, 3  
  
## See Also  
 [Interactive.InteractiveSession Class (F#)](../vs140/Interactive.InteractiveSession-Class--F#-.md)   
 [Microsoft.FSharp.Compiler.Interactive Namespace (F#)](../vs140/Microsoft.FSharp.Compiler.Interactive-Namespace--F#-.md)