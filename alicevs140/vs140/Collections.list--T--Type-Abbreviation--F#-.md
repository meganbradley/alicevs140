---
title: "Collections.list&lt;&#39;T&gt; Type Abbreviation (F#)"
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
  - Collections.list<'T> Type Abbreviation
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: dd7cd330-4bb6-4e28-b458-0ea62c6b0b04
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collections.list&lt;&#39;T&gt; Type Abbreviation (F#)
An abbreviation for [List](../vs140/Collections.List--T--Union--F#-.md), the type of immutable singly-linked lists.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type list<'T> = List<'T>  
```  
  
## Remarks  
 Use the constructors `[]` and `::` (infix) to create values of this type, or the notation `[1;2;3]`. Use the values in the [List module](../vs140/Collections.List-Module--F#-.md) to manipulate values of this type, or pattern match against the values directly.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)   
 [Collections.List Union (F#)](../vs140/Collections.List--T--Union--F#-.md)   
 [Collections.List Module](../vs140/Collections.List-Module--F#-.md)   
 [Lists (F#)](../Topic/Lists%20\(F%23\).md)