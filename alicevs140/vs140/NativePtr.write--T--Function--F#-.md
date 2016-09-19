---
title: "NativePtr.write&lt;&#39;T&gt; Function (F#)"
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
  - NativePtr.write<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c65eae26-60a8-4168-92cd-00ae36c9456a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NativePtr.write&lt;&#39;T&gt; Function (F#)
Assigns a value into the memory location referenced by the given typed native pointer.  
  
 **Namespace/Module Path:** Microsoft.FSharp.NativeInterop.NativePtr  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
NativePtr.write : nativeptr<'T> -> 'T -> unit (requires unmanaged)  
  
// Usage:  
NativePtr.write address value  
```  
  
#### Parameters  
 `address`  
 Type: [nativeptr](../vs140/Core.nativeptr--T--Type--F#-.md)`<'T>`  
  
 The input pointer.  
  
 `value`  
 Type: `'T`  
  
 The value to assign.  
  
## Remarks  
 This function is named `WritePointerInlined` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [NativeInterop.NativePtr Module (F#)](../vs140/NativeInterop.NativePtr-Module--F#-.md)   
 [Microsoft.FSharp.NativeInterop Namespace (F#)](../vs140/Microsoft.FSharp.NativeInterop-Namespace--F#-.md)