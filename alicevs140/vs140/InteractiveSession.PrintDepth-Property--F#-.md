---
title: "InteractiveSession.PrintDepth Property (F#)"
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
ms.assetid: 7d95a43a-e005-404c-bc7b-7014a7e96ade
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# InteractiveSession.PrintDepth Property (F#)
Gets or sets the print depth, or number of levels of recursive structures to print when displaying data, in the interactive session.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Compiler.Interactive  
  
 **Assembly:** FSharp.Compiler.Interactive.Settings (in FSharp.Compiler.Interactive.Settings.dll)  
  
## Syntax  
  
```  
// Signatures:  
member this.PrintDepth :  int  
member this.PrintDepth : int with set :  int  
  
// Usage:  
interactiveSession.PrintDepth  
interactiveSession.PrintDepth <- printDepth  
```  
  
#### Parameters  
 `printDepth`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
## Return Value  
  
## Remarks  
 The default value is 100.  
  
## Platforms  
 Windows 7, Windows Vista SP2, Windows XP SP3, Windows XP x64 SP2, Windows Server 2008 R2, Windows Server 2008 SP2, Windows Server 2003 SP2  
  
## Version Information  
 **F# Runtime**  
  
 Supported in: 2.0, 4  
  
 **Silverlight**  
  
 Supported in: 3  
  
## See Also  
 [Interactive.InteractiveSession Class (F#)](../vs140/Interactive.InteractiveSession-Class--F#-.md)   
 [Microsoft.FSharp.Compiler.Interactive Namespace (F#)](../vs140/Microsoft.FSharp.Compiler.Interactive-Namespace--F#-.md)