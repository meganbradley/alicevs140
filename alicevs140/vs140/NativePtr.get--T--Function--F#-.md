---
title: "NativePtr.get&lt;&#39;T&gt; Function (F#)"
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
  - NativePtr.get<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: eb9ac3e5-eef2-4914-aedf-7c60c7edccf2
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NativePtr.get&lt;&#39;T&gt; Function (F#)
Dereferences the typed native pointer computed by adding an offset to the given input pointer.  
  
 **Namespace/Module Path:** Microsoft.FSharp.NativeInterop.NativePtr  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
NativePtr.get : nativeptr<'T> -> int -> 'T (requires unmanaged)  
  
// Usage:  
NativePtr.get address index  
```  
  
#### Parameters  
 `address`  
 Type: [nativeptr](../vs140/Core.nativeptr--T--Type--F#-.md)`<'T>`  
  
 The input pointer.  
  
 `index`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index by which to offset the pointer.  
  
## Return Value  
 The value at the pointer address.  
  
## Remarks  
 The offset added to the pointer is `index * sizeof<'T>`.  
  
 This function is named `GetPointerInlined` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [NativeInterop.NativePtr Module (F#)](../vs140/NativeInterop.NativePtr-Module--F#-.md)   
 [Microsoft.FSharp.NativeInterop Namespace (F#)](../vs140/Microsoft.FSharp.NativeInterop-Namespace--F#-.md)