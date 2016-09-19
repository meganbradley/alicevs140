---
title: "ComPtr::CopyTo Method"
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
ms.assetid: 8801bc49-6db4-4393-a55f-a701ae3b8718
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtr::CopyTo Method
Copies the current or specified interface associated with this ComPtr to the specified pointer.  
  
## Syntax  
  
```  
HRESULT CopyTo(  
   _Deref_out_ InterfaceType** ptr  
);  
  
HRESULT CopyTo(  
   REFIID riid,  
   _Deref_out_ void** ptr  
) const;  
template<  
   typename U  
>  
  
HRESULT CopyTo(  
   _Deref_out_ U** ptr  
) const;  
```  
  
#### Parameters  
 `U`  
 A type name.  
  
 `ptr`  
 When this operation completes, a pointer to the requested interface.  
  
 `riid`  
 An interface ID.  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that indicates why the implicit QueryInterface operation failed.  
  
## Remarks  
 The first function returns a copy of a pointer to the interface associated with this ComPtr. This function always returns S_OK.  
  
 The second function performs a QueryInterface operation on the interface associated with this ComPtr for the interface specified by the `riid` parameter.  
  
 The third function performs a QueryInterface operation on the interface associated with this ComPtr for the underlying interface of the  `U` parameter.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ComPtr Class](../vs140/ComPtr-Class.md)