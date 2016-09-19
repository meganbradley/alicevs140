---
title: "WebRequest.AsyncGetResponse Extension Method (F#)"
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
apiname: 
  - WebRequest.AsyncGetResponse
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 09a60c31-e6e2-4b5c-ad23-92a86e50060c
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WebRequest.AsyncGetResponse Extension Method (F#)
Returns an asynchronous computation that, when run, will wait for a response to the given <xref:System.Net.WebRequest?qualifyHint=False>.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control.WebExtensions  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
type System.Net.WebRequest with  
  member AsyncGetResponse : unit -> Async<WebResponse>  
  
// Usage:  
webRequest.AsyncGetResponse ()  
```  
  
## Return Value  
 An asynchronous computation ([Async](../Topic/Control.Async%20Class%20\(F%23\).md) object) that waits for response to the web request.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0  
  
## See Also  
 <xref:System.Net.WebRequest?qualifyHint=False>   
 [Control.WebExtensions Module (F#)](../vs140/Control.WebExtensions-Module--F#-.md)