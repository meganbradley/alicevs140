---
title: "InteractiveSession.PrintLength Property (F#)"
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
ms.assetid: e4bc1b18-7623-48c3-9159-8c31019855c6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# InteractiveSession.PrintLength Property (F#)
Gets or sets the total print length, the number of elements to display when printing collection values, in the interactive session.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Compiler.Interactive  
  
 **Assembly:** FSharp.Compiler.Interactive.Settings (in FSharp.Compiler.Interactive.Settings.dll)  
  
## Syntax  
  
```  
// Signatures:  
member this.PrintLength :  int  
member this.PrintLength : int with set :  int  
  
// Usage:  
interactiveSession.PrintLength  
interactiveSession.PrintLength <- printLength  
```  
  
#### Parameters  
 `printLength`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The print length to set.  
  
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