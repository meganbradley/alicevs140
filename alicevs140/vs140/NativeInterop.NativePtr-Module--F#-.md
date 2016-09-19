---
title: "NativeInterop.NativePtr Module (F#)"
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
  - NativeInterop.NativePtr
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8d26f532-a190-4139-9722-c44f920c5e11
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NativeInterop.NativePtr Module (F#)
Contains operations on native pointers. Use of these operators may result in the generation of unverifiable code.  
  
 **Namespace/Module Path:** Microsoft.FSharp.NativeInterop  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module NativePtr  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[add](../vs140/NativePtr.add--T--Function--F#-.md)  `: nativeptr<'T> -> int -> nativeptr<'T>`|Returns a typed native pointer by adding an offset to the given input pointer.|  
|[get](../vs140/NativePtr.get--T--Function--F#-.md)  `: nativeptr<'T> -> int -> 'T`|Dereferences the typed native pointer computed by adding an offset to the given input pointer.|  
|[ofNativeInt](../vs140/NativePtr.ofNativeInt--T--Function--F#-.md)  `: nativeint -> nativeptr<'T>`|Returns a typed native pointer for a given machine address.|  
|[read](../vs140/NativePtr.read--T--Function--F#-.md)  `: nativeptr<'T> -> 'T`|Dereferences the given typed native pointer.|  
|[set](../vs140/NativePtr.set--T--Function--F#-.md)  `: nativeptr<'T> -> int -> 'T -> unit`|Assigns a value into the memory location referenced by the typed native pointer computed by adding an offset to the given input pointer.|  
|[stackalloc](../vs140/NativePtr.stackalloc--T--Function--F#-.md)  `: int -> nativeptr<'T>`|Allocates a region of memory on the stack.|  
|[toNativeInt](../vs140/NativePtr.toNativeInt--T--Function--F#-.md)  `: nativeptr<'T> -> nativeint`|Returns a machine address for a given typed native pointer.|  
|[write](../vs140/NativePtr.write--T--Function--F#-.md)  `: nativeptr<'T> -> 'T -> unit`|Assigns a value into the memory location referenced by the given typed native pointer.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.NativeInterop Namespace (F#)](../vs140/Microsoft.FSharp.NativeInterop-Namespace--F#-.md)