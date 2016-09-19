---
title: "ExtraTopLevelOperators.dict&lt;&#39;Key,&#39;Value&gt; Function (F#)"
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
  - ExtraTopLevelOperators.dict<'Key,'Value>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a8d7fac4-4466-44d9-bf31-7b29a21b2d17
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ExtraTopLevelOperators.dict&lt;&#39;Key,&#39;Value&gt; Function (F#)
Builds a read-only lookup table from a sequence of key/value pairs. The key objects are indexed using generic hashing and equality.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.ExtraTopLevelOperators  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
dict : seq<'Key * 'Value> -> IDictionary<'Key,'Value> (requires equality)  
  
// Usage:  
dict keyValuePairs  
```  
  
#### Parameters  
 `keyValuePairs`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'Key * 'Value>`  
  
## Return Value  
 An object that implements <xref:System.Collections.Generic.IDictionary`2?qualifyHint=False> that represents the given collection.  
  
## Remarks  
 This function is named `CreateDictionary` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example shows the use of the `dict` function.  
  
 [!CODE [FsCoreLib2#1](../CodeSnippet/VS_Snippets_Fsharp/fscorelib2#1)]  
  
 The output is as follows.  
  
 **The dictionary is read only.**  
**Value for key 5: 25**  
**Key: 1 Value: 1**  
**Key: 2 Value: 4**  
**Key: 3 Value: 9**  
**Key: 4 Value: 16**  
**Key: 5 Value: 25**  
**Key: 6 Value: 36**  
**Key: 7 Value: 49**  
**Key: 8 Value: 64**  
**Key: 9 Value: 81**  
**Key: 10 Value: 100**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.ExtraTopLevelOperators Module (F#)](../Topic/Core.ExtraTopLevelOperators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)