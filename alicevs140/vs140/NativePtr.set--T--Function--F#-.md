---
title: "NativePtr.set&lt;&#39;T&gt; Function (F#)"
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
  - NativePtr.set<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f232c376-3e92-4557-958d-f6c70aa739e0
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NativePtr.set&lt;&#39;T&gt; Function (F#)
Assigns a value into the memory location referenced by the typed native pointer computed by adding to the given input pointer.  
  
 **Namespace/Module Path:** Microsoft.FSharp.NativeInterop.NativePtr  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
NativePtr.set : nativeptr<'T> -> int -> 'T -> unit (requires unmanaged)  
  
// Usage:  
NativePtr.set address index value  
```  
  
#### Parameters  
 `address`  
 Type: [nativeptr](../vs140/Core.nativeptr--T--Type--F#-.md)`<'T>`  
  
 The input pointer.  
  
 `index`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index by which to offset the pointer.  
  
 `value`  
 Type: `'T`  
  
 The value to assign.  
  
## Remarks  
 The pointer is offset by `index * sizeof<'T>`.  
  
 This function is named `SetPointerInlined` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [NativeInterop.NativePtr Module (F#)](../vs140/NativeInterop.NativePtr-Module--F#-.md)   
 [Microsoft.FSharp.NativeInterop Namespace (F#)](../vs140/Microsoft.FSharp.NativeInterop-Namespace--F#-.md)