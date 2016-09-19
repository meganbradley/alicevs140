---
title: "CComSafeArray::Attach"
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
ms.assetid: 8396ced8-cf4e-4c0e-9a06-b3351fcfc9b0
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArray::Attach
Attaches a **SAFEARRAY** structure to a `CComSafeArray` object.  
  
## Syntax  
  
```  
  
      HRESULT Attach(  
   const SAFEARRAY * psaSrc   
);  
```  
  
#### Parameters  
 `psaSrc`  
 A pointer to the **SAFEARRAY** structure.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 Attaches a **SAFEARRAY** structure to a `CComSafeArray` object, making the existing `CComSafeArray` methods available.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArray Class](../vs140/CComSafeArray-Class.md)   
 [CComSafeArray::Detach](../vs140/CComSafeArray--Detach.md)