---
title: "WeakRef::CopyTo Method"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: f83de6da-b3d4-41a6-9845-cd725ecf3b75
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WeakRef::CopyTo Method
Assigns a pointer to an interface, if available, to the specified pointer variable.  
  
## Syntax  
  
```  
HRESULT CopyTo(  
   REFIID riid,  
   _Deref_out_ IInspectable** ptr  
);  
  
template<  
   typename U  
>  
HRESULT CopyTo(  
   _Deref_out_ U** ptr  
);  
  
HRESULT CopyTo(  
   _Deref_out_ IWeakReference** ptr  
);  
```  
  
#### Parameters  
 `U`  
 Pointer an IInspectable interface. An error is emitted if `U` is not derived from IInspectable.  
  
 `riid`  
 An interface ID. An error is emitted if `riid` is not derived from **IWeakReference**.  
  
 `ptr`  
 A doubly-indirect pointer to IInspectable or IWeakReference.  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that describes the failure. For more information, see Remarks.  
  
## Remarks  
 A return value of S_OK means that this operation succeeded, but doesn't indicate whether the weak reference was resolved to a strong reference. If S_OK is returned, test that parameter `p` is a strong reference; that is, parameter `p` isn't equal to `nullptr`.  
  
 Starting in the Windows 10 SDK, this method does not set the WeakRef instance to `nullptr` if the weak reference could not be obtained, so you should avoid error checking code that checks the WeakRef for `nullptr`. Instead, check `ptr` for `nullptr`.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WeakRef Class](../vs140/WeakRef-Class.md)