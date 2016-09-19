---
title: "CComPtrBase::Attach"
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
ms.assetid: 5f4b27d8-68de-493f-9da4-d15a12661d18
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtrBase::Attach
Call this method to take ownership of an existing pointer.  
  
## Syntax  
  
```  
  
      void Attach(  
   T* p2   
) throw( );  
```  
  
#### Parameters  
 `p2`  
 The `CComPtrBase` object will take ownership of this pointer.  
  
## Remarks  
 **Attach** calls [CComPtrBase::Release](../vs140/CComPtrBase--Release.md) on the existing [CComPtrBase::p](../vs140/CComPtrBase--p.md) member variable and then assigns `p2` to `CComPtrBase::p`. When a `CComPtrBase` object takes ownership of a pointer, it will automatically call `Release` on the pointer which will delete the pointer and any allocated data if the reference count on the object goes to 0.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtrBase Class](../vs140/CComPtrBase-Class.md)   
 [CComPtrBase::Detach](../vs140/CComPtrBase--Detach.md)