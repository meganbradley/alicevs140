---
title: "NativePtr.stackalloc&lt;&#39;T&gt; Function (F#)"
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
  - NativePtr.stackalloc<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a2c2855f-e4ff-4d10-b15a-e0fc3fecbb3d
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NativePtr.stackalloc&lt;&#39;T&gt; Function (F#)
Allocates a region of memory on the stack.  
  
 **Namespace/Module Path:** Microsoft.FSharp.NativeInterop.NativePtr  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
NativePtr.stackalloc : int -> nativeptr<'T> (requires unmanaged)  
  
// Usage:  
NativePtr.stackalloc count  
```  
  
#### Parameters  
 `count`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The number of objects of type T to allocate.  
  
## Return Value  
 A typed pointer to the allocated memory.  
  
## Remarks  
 This function is named `StackAllocate` in compiled assemblies. If you are accessing the member from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [NativeInterop.NativePtr Module (F#)](../vs140/NativeInterop.NativePtr-Module--F#-.md)   
 [Microsoft.FSharp.NativeInterop Namespace (F#)](../vs140/Microsoft.FSharp.NativeInterop-Namespace--F#-.md)